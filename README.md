<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Formación Ética y Ciudadana — 3° Año | Ciclo Lectivo 2026</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            institucional: { 50: '#f0f4f8', 100: '#d9e2ec', 500: '#2b6cb0', 700: '#1a365d', 800: '#102a43', 900: '#0a192f' }
          }
        }
      }
    }
  </script>
  <style>
    @media print {
      body * { visibility: hidden; }
      #area-impresion, #area-impresion * { visibility: visible; }
      #area-impresion { position: absolute; left: 0; top: 0; width: 100%; padding: 0; margin: 0; background: white !important; color: black !important; }
      .no-print { display: none !important; }
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-slate-900 dark:text-slate-100 font-sans antialiased transition-colors duration-200">

  <header class="bg-institucional-800 text-white shadow-lg sticky top-0 z-40 no-print">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-col md:flex-row md:items-center md:justify-between gap-4">
      <div>
        <div class="flex items-center gap-2 text-xs uppercase tracking-widest text-sky-300 font-semibold">
          <span>Provincia de Misiones • Educación Secundaria Orientada</span>
        </div>
        <h1 class="text-xl sm:text-2xl font-bold tracking-tight mt-0.5">Formación Ética y Ciudadana — 3.° Año</h1>
        <p class="text-xs text-slate-300 mt-0.5">Cuadernillo Pedagógico Interactivo • Prof. Alberto Carlos Frías • Ciclo Lectivo 2026</p>
      </div>
      <div class="flex items-center gap-3">
        <div class="relative w-full md:w-64">
          <input type="text" id="buscador-temas" placeholder="Buscar clase, ley o concepto..." class="w-full pl-9 pr-3 py-1.5 rounded-lg bg-institucional-900/80 border border-slate-600 text-sm text-white placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-sky-400" oninput="filtrarClases(this.value)">
          <svg class="w-4 h-4 text-slate-400 absolute left-3 top-2.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/></svg>
        </div>
        <button onclick="toggleDarkMode()" class="p-2 rounded-lg bg-institucional-700 hover:bg-institucional-500 text-amber-300 transition" title="Cambiar modo claro/oscuro">
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20"><path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"/></svg>
        </button>
      </div>
    </div>
  </header>

  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6 grid grid-cols-1 lg:grid-cols-12 gap-6 no-print">
    <aside class="lg:col-span-4 xl:col-span-3">
      <div class="bg-white dark:bg-slate-800 rounded-xl shadow-md border border-slate-200 dark:border-slate-700 overflow-hidden sticky top-24">
        <div class="bg-slate-100 dark:bg-slate-700/60 px-4 py-3 border-b border-slate-200 dark:border-slate-700 flex items-center justify-between">
          <h2 class="font-bold text-sm uppercase tracking-wider text-slate-700 dark:text-slate-200">Programa Anual (32 Clases)</h2>
          <span class="text-[11px] font-semibold px-2 py-0.5 rounded bg-emerald-100 dark:bg-emerald-900/50 text-emerald-800 dark:text-emerald-300">32 Completas</span>
        </div>
        <nav id="menu-unidades" class="divide-y divide-slate-200 dark:divide-slate-700 max-h-[75vh] overflow-y-auto"></nav>
      </div>
    </aside>
    <main class="lg:col-span-8 xl:col-span-9">
      <div id="contenedor-clase" class="bg-white dark:bg-slate-800 rounded-xl shadow-md border border-slate-200 dark:border-slate-700 p-6 sm:p-8"></div>
    </main>
  </div>

  <div id="area-impresion" class="hidden print:block p-8 text-black bg-white">
    <div id="contenido-imprimible"></div>
  </div>

  <script>
    const programaCurricular = [
      {
        id: "u1", numero: "Unidad 1", titulo: "La Dimensión Ética", activa: true,
        clases: [
          {
            id: "c1", numero: "Clase 1", titulo: "Introducción a la Ética y la Moral", desarrollada: true,
            normativa: "Principios Generales de Convivencia Social y Deberes Cívicos • Ordenamiento Constitucional Argentino",
            teoria: [
              "En nuestra materia comenzamos distinguiendo dos conceptos fundamentales que suelen usarse como sinónimos pero tienen alcances distintos. La <strong>moral</strong> (conjunto normativo, consuetudinario y valórico de una comunidad, es decir, el sistema de reglas, costumbres y valores que una sociedad adopta históricamente para regular la convivencia diaria y señalar qué conductas son correctas o incorrectas) funciona como una guía práctica inmediata en la familia, el barrio y la escuela.",
              "Por su parte, la <strong>ética</strong> (disciplina filosófica de segundo orden, lo que significa que es una rama de la filosofía que somete a examen crítico, reflexivo y racional los preceptos de la moral vigente) analiza por qué consideramos justas o buenas determinadas acciones. Mientras la moral responde a la pregunta práctica sobre <em>qué debo hacer</em>, la ética indaga sobre <em>por qué debo hacerlo</em>, buscando fundamentos racionales y universales.",
              "En la vida escolar distinguimos así entre la <strong>moral vivida</strong> (cumplir normas aprendidas por tradición o socialización) y la <strong>ética reflexiva</strong> (el ejercicio intelectual de evaluar la justicia y validez universal de esas normas). Comprender esta diferencia nos permite pasar de obedecer reglas mecánicamente a sostener principios basados en la dignidad humana."
            ],
            cuadro: {
              columnas: ["Dimensión de Análisis", "Moral (Moral Vivida)", "Ética (Ética Reflexiva)"],
              filas: [
                ["Concepto Técnico y Sencillo", "Conjunto consuetudinario de normas y costumbres (reglas prácticas adoptadas históricamente por un grupo).", "Disciplina filosófica de segundo orden (reflexión crítica, sistemática y racional sobre las normas morales)."],
                ["Nivel de Actuación", "Práctico e inmediato: regula los actos cotidianos indicando qué es correcto o incorrecto.", "Teórico y fundamentador: indaga por qué una norma es justa o universalmente válida."],
                ["Origen de la Norma", "Social, cultural e histórico: se transmite por tradición, hábitos y crianza comunitaria.", "Racional y filosófico: exige argumentación lógica y examen crítico autónomo."],
                ["Ejemplo Cotidiano", "Devolver una billetera encontrada en la calle porque así nos enseñaron que actúa alguien honrado.", "Analizar por qué la honestidad y el respeto a la propiedad ajena son indispensables para la confianza social."]
              ]
            },
            caso: {
              titulo: "El hallazgo en el patio del colegio durante el recreo",
              relato: "Durante el segundo recreo en un colegio secundario de Oberá, un grupo de estudiantes de 3.° año encuentra cerca del kiosco escolar una billetera sin identificación con el dinero que un alumno de primer año trajo para su pasaje y útiles. Uno sugiere repartirse el dinero diciendo que 'encontrar algo sin nombre no es robar'. Otro compañero se opone y sostiene que deben entregarla en Preceptoría, no solo porque el acuerdo escolar lo exige, sino porque quedarse con algo ajeno daña a un compañero y destruye la confianza en la escuela.",
              preguntaGuia: "¿Cuál de las posturas se limita a una excusa circunstancial y cómo aparece en el segundo compañero el paso de la norma moral al fundamento ético?"
            },
            actividades: [
              "<strong>Precisión Conceptual:</strong> Redactá con tus palabras la diferencia fundamental entre <em>moral vivida</em> (costumbre práctica) y <em>ética reflexiva</em> (examen racional), explicando por qué se complementan.",
              "<strong>Análisis del Caso Escolar:</strong> Identificá cuál es la norma moral en juego en el hallazgo de la billetera y redactá el argumento ético racional que justifica por qué restituirla es un deber comunitario.",
              "<strong>Aplicación Institucional:</strong> Enunciá dos normas morales vigentes en tu escuela o tu hogar y justificá racionalmente por qué son necesarias para una convivencia armónica."
            ]
          },
          {
            id: "c2", numero: "Clase 2", titulo: "Autonomía y Heteronomía Moral", desarrollada: true,
            normativa: "Desarrollo del Juicio Moral (Piaget / Kohlberg) • Principio de Autodeterminación y Ciudadanía Democrática",
            teoria: [
              "A medida que crecemos y transitamos la adolescencia, evoluciona el modo en que nos vinculamos con las normas. Llamamos <strong>heteronomía moral</strong> (condición en la cual la voluntad del sujeto está supeditada a determinaciones o coacciones externas, es decir, cuando se cumple una regla solo por imposición de otro, por miedo al castigo o para obtener premios o aprobación grupal) a la etapa en que el control proviene desde afuera.",
              "En contraposición, la <strong>autonomía moral</strong> (capacidad del individuo de autodeterminarse conforme a principios universales dictados por la razón práctica y la convicción interior, eligiendo hacer lo correcto porque comprende racionalmente su valor ético) constituye la meta de la madurez ciudadana. Quien es autónomo obra rectamente incluso sin vigilancia.",
              "En la convivencia democrática, superar los <strong>factores exógenos de control</strong> (las presiones externas como la mirada punitiva) para alcanzar la <strong>autorregulación moral</strong> (el gobierno consciente de la propia conducta fundado en el juicio crítico) resulta indispensable para construir una sociedad libre y responsable."
            ],
            cuadro: {
              columnas: ["Criterio Comparativo", "Heteronomía Moral", "Autonomía Moral"],
              filas: [
                ["Significado Etimológico y Técnico", "Ley que proviene de otro (voluntad condicionada por mandatos o presiones externas).", "Ley que uno se da a sí mismo (autodeterminación racional fundada en convicciones éticas propias)."],
                ["Motivación de la Conducta", "Temor a la sanción punitiva, búsqueda de recompensa o sumisión acrítica a una autoridad o grupo.", "Convicción interior, respeto a la dignidad humana y comprensión racional del deber."],
                ["Dependencia de Vigilancia", "Requiere fiscalización externa: si desaparece el control, suele transgredirse la norma.", "Independiente de vigilancia: la conducta justa se mantiene aunque nadie observe."],
                ["Ejemplo en el Aula", "No copiarse en una prueba únicamente porque el docente está mirando fijamente el banco.", "No copiarse por respeto al propio aprendizaje y al valor de la honestidad intelectual."]
              ]
            },
            caso: {
              titulo: "La evaluación escrita y el aula sin vigilancia",
              relato: "Durante una evaluación de Formación Ética en 3.° año, el profesor debe salir del salón tres minutos por un llamado urgente de Dirección. Apenas se cierra la puerta, varios alumnos sacan celulares y apuntes diciendo: 'Aprovechen ahora que el profe no nos ve'. Sin embargo, Sofía y Mateo mantienen sus carpetas cerradas y resuelven el examen solo con lo que estudiaron, sosteniendo que engañar en la prueba es engañarse a sí mismos.",
              preguntaGuia: "¿Cómo se manifiestan la heteronomía y la autonomía moral en la reacción de los distintos alumnos cuando desaparece la vigilancia externa?"
            },
            actividades: [
              "<strong>Fundamentación Ciudadana:</strong> Explicá por qué alcanzar la <em>autonomía moral</em> (autodeterminación racional) es indispensable para ejercer la ciudadanía en democracia.",
              "<strong>Resolución del Dilema Áulico:</strong> Analizá el caso de la evaluación sin vigilancia docente y clasificá las conductas explicando qué factores externos (exógenos) o internos guiaron a cada grupo.",
              "<strong>Transición Experiencial:</strong> Desarrollá un ejemplo cotidiano de un joven de 15 años donde se evidencie el paso de una conducta <em>heterónoma</em> a una decisión plenamente <em>autónoma</em>."
            ]
          },
          {
            id: "c3", numero: "Clase 3", titulo: "Libertad y Responsabilidad", desarrollada: true,
            normativa: "Art. 19 de la Constitución Nacional • Art. 260 del Código Civil y Comercial de la Nación (Acto Voluntario)",
            teoria: [
              "En Formación Ética y Ciudadana establecemos que la <strong>libertad</strong> (facultad consciente de elegir y autodeterminarse entre distintas alternativas de acción) nunca es absoluta ni ilimitada en la vida social. El artículo 19 de la Constitución Nacional consagra que la libertad de cada persona halla su límite en el orden público y en los derechos de terceros; actuar desconociendo esos límites degrada la libertad en <strong>libertinaje</strong> (ejercicio abusivo e irresponsable que lesiona derechos ajenos).",
              "Por ello, la contrapartida inseparable de la libertad es la <strong>responsabilidad</strong> (del latín <em>respondere</em>: obligación ética y jurídica ineludible de dar cuenta, asumir las consecuencias de nuestras decisiones y reparar los daños causados). Ambas conforman una <strong>relación dialéctica</strong> (vínculo de mutua dependencia donde soy responsable porque elegí libremente).",
              "Según el artículo 260 del Código Civil y Comercial de la Nación, para que una acción configure un <strong>acto voluntario</strong> (conducta imputable) deben concurrir tres elementos internos: <strong>discernimiento</strong> (madurez y aptitud mental para comprender el acto), <strong>intención</strong> (propósito consciente de realizarlo) y <strong>libertad</strong> (obrar sin coacción física ni amenazas ilegítimas)."
            ],
            cuadro: {
              columnas: ["Concepto / Elemento", "Definición Técnica y Precisión Conceptual", "Límite o Consecuencia Práctica"],
              filas: [
                ["Libertad", "Facultad de autodeterminación consciente entre diversas opciones de conducta.", "Termina donde comienzan las leyes vigentes y los derechos de los demás (Art. 19 C.N.)."],
                ["Responsabilidad", "Deber ético y jurídico de responder, dar cuenta y asumir los efectos del propio obrar.", "Implica afrontar las consecuencias académicas, sociales o legales y reparar perjuicios."],
                ["Acto Voluntario (Art. 260 CCyCN)", "Concurrencia de: 1) Discernimiento (comprender), 2) Intención (querer) y 3) Libertad (sin coacción).", "Reunidos los tres elementos, el sujeto responde plenamente por los resultados de su acción."],
