// ==========================================
// SVNU YEAR 2 (SEMESTER 1) - HARVESTED ACADEMIC DATA
// ==========================================
window.MEDAI_SVNU_BLOCKS = {
  SMU: {
    title: "Skin & Musculoskeletal Module",
    lectures: [
      { id: "smu_lec_01", title: "Muscles of the Upper Limb - Part 1", file: "fr anatomy lecture.mp3" },
      { id: "smu_lec_02", title: "Muscles of the Upper Limb - Part 2", file: "Voice 001.m4a" }
    ],
    clinicalCases: [
      {
        id: "case_smu_01",
        presentation: "A 45-year-old woman presents with a 4-month history of progressive, symmetrical weakness in her shoulders and hips. She struggles to lift her arms above her head and climb stairs. Examination confirms proximal muscle weakness with no skin rash. Laboratory tests reveal elevated Creatine Kinase (CK) and positive Antinuclear Antibodies (ANA). EMG displays myopathic changes.",
        question: "Which diagnostic investigation is most likely to confirm the suspected diagnosis?",
        diagnosis: "Polymyositis",
        confirmatoryInvestigation: "Muscle Biopsy"
      },
      {
        id: "case_smu_02",
        presentation: "A 62-year-old woman presents with proximal limb weakness, difficulty rising from a chair, and a purplish-red discoloration around her eyes (heliotrope rash). Physical exam also reveals erythematous papules over the metacarpophalangeal joints (Gottron's papules) and extensor surfaces.",
        question: "What is the most likely diagnosis?",
        diagnosis: "Dermatomyositis",
        confirmatoryInvestigation: "Muscle Biopsy & Clinical Presentation"
      }
    ],
    highYieldExamPoints: [
      "Median Nerve Entrapment: The most common site of compression is the Carpal Tunnel beneath the flexor retinaculum.",
      "Platelet Pathophysiology: Defect in platelet adhesion = Bernard-Soulier syndrome (GpIb deficiency); Defect in platelet aggregation = Glanzmann thrombasthenia (GpIIb/IIIa deficiency).",
      "Henoch-Schönlein Purpura (HSP): The most common pediatric vasculitis. An acute IgA-mediated disorder presenting with palpable purpura on the extensor surfaces of lower limbs and buttocks, with normal platelet counts.",
      "Immune Thrombocytopenic Purpura (ITP): Platelet transfusion is strictly contraindicated as transfused platelets are rapidly cleared by circulating antiplatelet autoantibodies."
    ]
  },

  GIT: {
    title: "Gastrointestinal Tract Module",
    topics: [
      {
        condition: "Wilson's Disease (Hepatolenticular Degeneration)",
        etiology: "Autosomal recessive disorder of impaired copper metabolism, leading to pathological copper deposition in the basal ganglia and liver.",
        clinicalTriad: "Hepatic dysfunction, neuropsychiatric symptoms, and Kayser-Fleischer (KF) corneal rings.",
        investigations: "Decreased serum ceruloplasmin and elevated quantitative copper concentration on liver biopsy.",
        management: "Copper chelating agents (Penicillamine, Trientine), oral Zinc, and liver transplantation in fulminant cases."
      }
    ],
    clinicalCases: [
      {
        id: "case_git_01",
        presentation: "A 28-year-old male presents to the Emergency Department with symmetrical, progressive ascending flaccid weakness starting in his lower extremities. Deep tendon reflexes (DTRs) are absent bilaterally. Two weeks prior, he suffered an acute gastrointestinal diarrheal illness. He is now developing mild respiratory distress.",
        question: "What is the most critical next step in management?",
        diagnosis: "Guillain-Barré Syndrome (Acute Inflammatory Demyelinating Polyradiculoneuropathy)",
        immediateAction: "Assess respiratory mechanics via Forced Vital Capacity (FVC) / Negative Inspiratory Force (NIF) to anticipate mechanical ventilation, followed by IVIG or Plasmapheresis."
      }
    ]
  },

  Urinary: {
    title: "Renal & Urinary System Module",
    pediatricOncologyComparison: {
      wilmsTumor: {
        presentation: "Smooth, firm, unilateral abdominal flank mass that typically does NOT cross the anatomical midline.",
        indicationsForPartialNephrectomy: ["Bilateral Wilms' tumors", "Tumor in a solitary anatomical kidney"],
        workup: "Abdominal Ultrasound, Abdominal CT/MRI, and Chest CT/Radiograph to evaluate pulmonary metastases."
      },
      neuroblastoma: {
        presentation: "Hard, irregular, nodular abdominal mass that CROSSES the anatomical midline. May present with proptosis and periorbital ecchymosis.",
        laboratoryMarkers: "Markedly elevated urinary catecholamine metabolites: Vanillylmandelic acid (VMA) and Homovanillic acid (HVA)."
      }
    },
    writtenCoreTopics: [
      "Nephrotic Syndrome: Classic triad of massive proteinuria (>40 mg/m²/hr), profound hypoalbuminemia (<2.5 g/dL), and generalized dependent edema.",
      "Congenital Adrenal Hyperplasia (CAH): Workup for Disorders of Sex Development (DSD), including karyotyping, 17-hydroxyprogesterone levels, serum electrolytes, and pelvic ultrasound."
    ]
  },

  ECE2: {
    title: "Early Clinical Experience 2 (ECE 2)",
    clinicalCases: [
      {
        id: "case_ece_01",
        presentation: "A 30-year-old female presents with fluctuating diplopia and bilateral ptosis that worsens towards the end of the day and improves markedly upon waking. She notes chewing fatigue during meals. An ice pack test applied to the orbits produces temporary improvement in ptosis. Anti-AChR autoantibody serology is positive.",
        question: "What is the primary first-line symptomatic pharmacological management?",
        diagnosis: "Myasthenia Gravis (Postsynaptic NMDA/AChR defect)",
        firstLineTherapy: "Oral Pyridostigmine (Acetylcholinesterase inhibitor)"
      }
    ],
    pharmacologyProtocols: [
      "Amantadine in Parkinsonism: Acts by enhancing endogenous dopamine release, inhibiting dopamine reuptake, and exerting non-competitive NMDA receptor antagonism; primarily alleviates bradykinesia and rigidity.",
      "Stepwise Management of Generalized Dystonia: 1) Diagnostic trial of oral Levodopa (to exclude dopa-responsive dystonia) -> 2) Anticholinergic therapy (Benztropine/Trihexyphenidyl) -> 3) High-dose Benzodiazepines or Tetrabenazine -> 4) Localized Botulinum Toxin Type A injections for focal dystonic spasms."
    ]
  }
};

// Auto-injection into MedAI Dashboard
function mountEnglishModules() {
  const mountPoint = document.getElementById('svnu-harvested-root') || document.querySelector('main');
  if (!mountPoint || document.getElementById('medai-en-blocks')) return;

  const panel = document.createElement('div');
  panel.id = 'medai-en-blocks';
  panel.className = 'bg-slate-900 border border-slate-800 rounded-3xl p-6 text-white space-y-4 shadow-xl my-6';
  panel.dir = 'ltr'; // Set to LTR for standard English reading

  let html = `
    <div class="flex items-center justify-between border-b border-slate-800 pb-3">
      <h3 class="text-sm font-bold text-emerald-400 flex items-center gap-2">
        <span>Academic Year 2 Modules (Integrated English Curriculum)</span>
      </h3>
      <span class="text-[10px] bg-emerald-950 text-emerald-300 border border-emerald-800 px-2 py-0.5 rounded-full font-mono">SVNU Academic</span>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-3 text-left">
  `;

  for (const [key, block] of Object.entries(window.MEDAI_SVNU_BLOCKS)) {
    html += `
      <div class="bg-slate-800/80 border border-slate-700/70 p-4 rounded-2xl space-y-2">
        <div class="flex items-center justify-between">
          <span class="bg-emerald-600 text-slate-950 text-[10px] font-black px-2 py-0.5 rounded-md font-mono">${key}</span>
        </div>
        <h4 class="text-xs font-bold text-white">${block.title}</h4>
        <div class="text-[11px] text-slate-300 space-y-1 pt-1 font-sans">
          ${block.lectures ? `<p>🎙️ Audio Lectures: <span class="text-emerald-400 font-bold">${block.lectures.length}</span></p>` : ''}
          ${block.clinicalCases ? `<p>🩺 Clinical Cases: <span class="text-cyan-400 font-bold">${block.clinicalCases.length}</span></p>` : ''}
          ${block.highYieldExamPoints ? `<p>⚡ High-Yield Facts: <span class="text-amber-400 font-bold">${block.highYieldExamPoints.length}</span></p>` : ''}
          ${block.topics ? `<p>🧪 Key Disorders: <span class="text-emerald-400 font-bold">${block.topics.length}</span></p>` : ''}
          ${block.pediatricOncologyComparison ? `<p class="text-purple-400 font-bold">⚖️ Comparative Tables</p>` : ''}
        </div>
      </div>
    `;
  }

  html += `</div>`;
  panel.innerHTML = html;
  mountPoint.prepend(panel);
}

if (document.readyState === 'loading') {
  document.addEventListener('DOMContentLoaded', mountEnglishModules);
} else {
  mountEnglishModules();
}
