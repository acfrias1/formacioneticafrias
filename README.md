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
            institucional: {
              50: '#f0f4f8',
              100: '#d9e2ec',
              500: '#2b6cb0',
              700: '#1a365d',
              800: '#102a43',
              900: '#0a192f',
            }
          }
        }
      }
    }
  </script>
  <style>
    @media print {
      body * { visibility: hidden; }
      #area-impresion, #area-impresion * { visibility: visible; }
      #area-impresion {
        position: absolute; left: 0; top: 0; width: 100%;
        padding: 0; margin: 0; background: white !important; color: black !important;
      }
      .no-print { display: none !important; }
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-slate-900 dark:text-slate-100 font-sans antialiased transition-colors duration-200">

  <!-- ENCABEZADO INSTITUCIONAL SUPERIOR -->
  <header class="bg-institucional-800 text-white shadow-lg sticky top-0 z-40 no-print">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-col md:flex-row md:items-center md:justify-between gap-4">
      <div>
        <div class="flex items-center gap-2 text-xs uppercase tracking-widest text-sky-300 font-semibold">
          <span>Provincia de Misiones • Educación Secundaria Orientada</span>
        </div>
        <h1 class="text-xl sm:text-2xl font-bold tracking-tight mt-0.5">
          Formación Ética y Ciudadana — 3.° Año
        </h1>
        <p class="text-xs text-slate-300 mt-0.5">
          Cuadernillo Pedagógico Interactivo • Prof. Alberto Carlos Frías • Ciclo Lectivo 2026
        </p>
      </div>

      <div class="flex items-center gap-3">
        <div class="relative w-full md:w-64">
          <input 
            type="text" 
            id="buscador-temas" 
            placeholder="Buscar clase, ley o concepto..." 
            class="w-full pl-9 pr-3 py-1.5 rounded-lg bg-institucional-900/80 border border-slate-600 text-sm text-white placeholder-slate-400 focus:outline-none focus:ring-2 focus:ring-sky-400"
            oninput="filtrarClases(this.value)"
          >
          <svg class="w-4 h-4 text-slate-400 absolute left-3 top-2.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/>
          </svg>
        </div>

        <button 
          onclick="toggleDarkMode()" 
          class="p-2 rounded-lg bg-institucional-700 hover:bg-institucional-500 text-amber-300 transition"
          title="Cambiar modo claro/oscuro"
        >
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
            <path d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"/>
          </svg>
        </button>
      </div>
    </div>
  </header>

  <!-- CONTENEDOR PRINCIPAL -->
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6 grid grid-cols-1 lg:grid-cols-12 gap-6 no-print">

    <!-- MENÚ LATERAL DE UNIDADES Y CLASES -->
    <aside class="lg:col-span-4 xl:col-span-3">
      <div class="bg-white dark:bg-slate-800 rounded-xl shadow-md border border-slate-200 dark:border-slate-700 overflow-hidden sticky top-24">
        <div class="bg-slate-100 dark:bg-slate-700/60 px-4 py-3 border-b border-slate-200 dark:border-slate-700 flex items-center justify-between">
          <h2 class="font-bold text-sm uppercase tracking-wider text-slate-700 dark:text-slate-200">
            Programa Anual (32 Clases)
          </h2>
          <span class="text-[11px] font-semibold px-2 py-0.5 rounded bg-emerald-100 dark:bg-emerald-900/50 text-emerald-800 dark:text-emerald-300">
            100% Completo
          </span>
        </div>
        <nav id="menu-unidades" class="divide-y divide-slate-200 dark:divide-slate-700 max-h-[75vh] overflow-y-auto"></nav>
      </div>
    </aside>

    <!-- ÁREA CENTRAL DE CONTENIDO DE LA CLASE -->
    <main class="lg:col-span-8 xl:col-span-9">
      <div id="contenedor-clase" class="bg-white dark:bg-slate-800 rounded-xl shadow-md border border-slate-200 dark:border-slate-700 p-6 sm:p-8"></div>
    </main>

  </div>

  <!-- ÁREA OCULTA FORMATEADA EXCLUSIVAMENTE PARA IMPRESIÓN / PDF A4 DEL ALUMNO -->
  <div id="area-impresion" class="hidden print:block p-8 text-black bg-white">
    <div id="contenido-imprimible"></div>
  </div>

  <!-- BASE DE DATOS ÍNTEGRA SIN RECORTES DE LAS 32 CLASES DEL CUADERNO ÉTICA 2026 -->
  <script>
    const programaCurricular = [
      {
        id: "u1",
        numero: "Unidad 1",
        titulo: "La Dimensión Ética",
        activa: true,
        clases: [
          {
            id: "c1",
            numero: "Clase 1",
            titulo: "Introducción a la Ética y la Moral",
            desarrollada: true,
            normativa: "Principios Generales de Convivencia Social y Deberes Cívicos • Ordenamiento Constitucional Argentino",
            teoria: [
              "En el estudio de nuestra asignatura comenzamos distinguiendo dos conceptos fundamentales que suelen confundirse en el lenguaje cotidiano pero que poseen alcances diferentes. La <strong>moral</strong> (conjunto normativo, consuetudinario y valórico de una comunidad, es decir, el sistema de reglas, costumbres, hábitos y valores que una sociedad construye históricamente para regular la convivencia diaria y señalar qué conductas se consideran correctas o incorrectas) funciona como una guía práctica e inmediata en nuestra vida familiar, barrial y escolar.",
              "Por su parte, la <strong>ética</strong> (disciplina filosófica de segundo orden, lo que significa que es una rama de la filosofía que no impone reglas por mera tradición, sino que somete a un examen crítico, reflexivo y sistemático los preceptos de la moral vigente) se encarga de analizar racionalmente por qué consideramos buenas o justas determinadas acciones. Mientras la moral responde a la pregunta práctica sobre <em>qué debo hacer</em>, la ética indaga sobre <em>por qué debo hacerlo</em>, buscando fundamentos universales para el obrar humano.",
              "En la convivencia escolar e institucional distinguimos así entre la <strong>moral vivida</strong> (la práctica habitual de cumplir normas aprendidas por socialización) y la <strong>ética reflexiva</strong> (el ejercicio intelectual de evaluar la justicia y validez racional de esas normas). Comprender esta diferencia nos permite pasar de obedecer reglas de manera mecánica a sostener principios de convivencia basados en la dignidad humana."
            ],
            cuadro: {
              columnas: ["Dimensión de Análisis", "Moral (Moral Vivida)", "Ética (Ética Reflexiva)"],
              filas: [
                ["Concepto Técnico y Sencillo", "Conjunto consuetudinario de normas y costumbres (reglas prácticas adoptadas históricamente por un grupo).", "Disciplina filosófica de segundo orden (reflexión crítica, sistemática y racional sobre las normas morales)."],
                ["Nivel de Actuación", "Práctico e inmediato: regula los actos cotidianos indicando qué es correcto o incorrecto.", "Teórico y fundamentador: indaga por qué una norma es justa o universalmente válida."],
                ["Origen de la Norma", "Social, cultural e histórico: se transmite por tradición, hábitos y crianza comunitaria.", "Racional y filosófico: exige argumentación lógica y examen crítico autónomo."],
                ["Ejemplo Cotidiano", "Devolver una billetera encontrada en la vía pública porque así nos enseñaron que actúa alguien honrado.", "Analizar por qué la honestidad y el respeto recíproco son pilares indispensables para la confianza social."]
              ]
            },
            caso: {
              titulo: "El hallazgo en el patio del colegio durante el recreo",
              relato: "Durante el segundo recreo en el colegio secundario de Oberá, un grupo de estudiantes de 3.° año encuentra cerca del kiosco escolar una billetera sin identificación que contiene el dinero exacto que un alumno de primer año había traído para pagar su pasaje de colectivo y comprar útiles. Uno de los jóvenes sugiere repartirse el dinero argumentando que 'el que encuentra algo en el piso sin nombre no está robando'. Otro compañero se opone y sostiene que deben entregarla en Preceptoría, no solo porque el acuerdo escolar de convivencia lo exige, sino porque quedarse con algo ajeno daña directamente a un compañero y destruye la confianza dentro de la escuela.",
              preguntaGuia: "¿Cuál de las posturas se limita a una excusa circunstancial y cómo aparece en el segundo compañero el paso de la norma moral al fundamento ético?"
            },
            actividades: [
              "<strong>Precisión Conceptual:</strong> Redactá con tus propias palabras la diferencia fundamental entre <em>moral vivida</em> (costumbre práctica) y <em>ética reflexiva</em> (examen racional), explicando por qué ambas se complementan en la vida ciudadana.",
              "<strong>Análisis del Caso Escolar:</strong> A partir del caso leído sobre el hallazgo de la billetera en el recreo, identificá cuál es la norma moral en juego y redactá el argumento ético racional que justifica por qué restituir el objeto a su dueño es un deber hacia la comunidad escolar.",
              "<strong>Aplicación Institucional:</strong> Enunciá dos normas morales o pautas de conducta que cumplas habitualmente en la escuela o en tu hogar y justificá racionalmente por qué son justas y necesarias para sostener una convivencia armónica."
            ]
          },
          {
            id: "c2",
            numero: "Clase 2",
            titulo: "Autonomía y Heteronomía Moral",
            desarrollada: true,
            normativa: "Desarrollo del Juicio Moral • Principio de Autodeterminación y Ciudadanía Democrática",
            teoria: [
              "A medida que crecemos y transitamos la adolescencia, evoluciona el modo en que nos vinculamos con las normas. Llamamos <strong>heteronomía moral</strong> (condición en la cual la voluntad del sujeto se encuentra supeditada a determinaciones o coacciones externas, es decir, cuando una persona actúa o cumple una regla únicamente por imposición de otro, por miedo al castigo, por temor a una sanción o para obtener la aprobación del grupo) a la etapa en que el control de la conducta proviene desde afuera.",
              "En contraposición, la <strong>autonomía moral</strong> (capacidad del individuo maduro de autodeterminarse conforme a principios universales dictados por la razón práctica y la convicción interior, lo que significa gobernarse a sí mismo eligiendo hacer lo correcto porque comprende racionalmente su valor ético) constituye la meta de la formación ciudadana. Quien actúa con autonomía cumple con su deber ético incluso cuando nadie lo está vigilando.",
              "En la vida democrática y escolar, superar los <strong>factores exógenos de control</strong> (las presiones externas como la vigilancia punitiva o la mirada ajena) para alcanzar la <strong>autorregulación moral</strong> (el gobierno consciente de la propia conducta fundado en el juicio crítico) resulta indispensable: una democracia sólida no se sostiene con ciudadanos que solo respetan la ley cuando ven a una autoridad, sino con sujetos autónomos comprometidos con el bien común."
            ],
            cuadro: {
              columnas: ["Criterio Comparativo", "Heteronomía Moral", "Autonomía Moral"],
              filas: [
                ["Significado Etimológico y Técnico", "Ley que proviene de otro (voluntad condicionada por mandatos o presiones externas).", "Ley que uno se da a sí mismo (autodeterminación racional fundada en convicciones éticas propias)."],
                ["Motivación de la Conducta", "Temor al castigo, búsqueda de premios o sumisión acrítica a una autoridad o grupo.", "Convicción interior, respeto a la dignidad humana y comprensión racional del deber."],
                ["Dependencia de Vigilancia", "Requiere control externo permanente: si desaparece la vigilancia, se transgrede la norma.", "Independiente de vigilancia: la conducta justa se sostiene aunque nadie observe."],
                ["Ejemplo en el Aula", "No copiarse en una evaluación escrita únicamente porque el docente está mirando fijamente el banco.", "No copiarse por respeto al propio proceso de aprendizaje y al valor de la honestidad académica."]
              ]
            },
            caso: {
              titulo: "La evaluación escrita y el aula sin vigilancia",
              relato: "Durante una evaluación trimestral de Formación Ética y Ciudadana en 3.° año, el profesor debe retirarse del salón por tres minutos ante un llamado urgente de la Dirección. Apenas se cierra la puerta, varios estudiantes sacan sus teléfonos celulares y apuntes ocultos para copiar las respuestas, diciendo en voz baja: 'Aprovechen ahora que el profe no nos ve y no nos puede sacar la hoja'. Sin embargo, Sofía y Mateo deciden mantener sus carpetas cerradas y resolver el examen únicamente con lo que estudiaron, sosteniendo que engañar en la prueba equivale a engañarse a sí mismos.",
              preguntaGuia: "¿Cómo se manifiestan la heteronomía y la autonomía moral en la reacción de los distintos alumnos cuando desaparece la vigilancia externa?"
            },
            actividades: [
              "<strong>Fundamentación Ciudadana:</strong> Explicá por qué alcanzar la <em>autonomía moral</em> (autodeterminación por convicción racional) es un requisito indispensable para el ejercicio pleno de la ciudadanía en un sistema democrático.",
              "<strong>Resolución del Dilema Áulico:</strong> Analizá el caso de la evaluación sin vigilancia docente y clasificá las conductas de los estudiantes explicando qué factores externos (exógenos) o internos guiaron a cada grupo.",
              "<strong>Transición Experiencial:</strong> Desarrollá un ejemplo concreto de la vida cotidiana de un joven de 15 años donde se evidencie el paso desde una conducta <em>heterónoma</em> hacia una decisión plenamente <em>autónoma</em>, indicando qué valores personales motivaron ese cambio."
            ]
          },
          {
            id: "c3",
            numero: "Clase 3",
            titulo: "Libertad y Responsabilidad",
            desarrollada: true,
            normativa: "Art. 19 de la Constitución Nacional • Art. 260 del Código Civil y Comercial de la Nación (Acto Voluntario)",
            teoria: [
              "En Formación Ética y Ciudadana establecemos que la <strong>libertad</strong> (facultad consciente de elegir y autodeterminarse entre distintas alternativas de acción, es decir, la capacidad humana de decidir con conciencia qué hacer o no hacer) nunca es absoluta ni ilimitada en la vida social. Nuestro ordenamiento jurídico consagra en el artículo 19 de la Constitución Nacional que la libertad de cada persona halla su límite infranqueable en el orden público, la moral y los derechos de terceros; actuar desconociendo esos límites degrada la libertad en <strong>libertinaje</strong> (ejercicio abusivo e irresponsable que lesiona derechos ajenos).",
              "Por ello, la contrapartida inseparable de la libertad es la <strong>responsabilidad</strong> (del latín <em>respondere</em>, que significa obligación ética y jurídica ineludible de dar cuenta, asumir plenamente las consecuencias de nuestras decisiones y reparar los daños causados). Libertad y responsabilidad conforman una <strong>relación dialéctica</strong> (un vínculo de mutua dependencia donde no existe una sin la otra): solo soy responsable de aquello que elegí libremente, y porque soy libre debo hacerme cargo de los resultados de mis actos.",
              "Conforme al artículo 260 del Código Civil y Comercial de la Nación, para que una acción configure un <strong>acto voluntario</strong> (conducta imputable que genera responsabilidad) deben concurrir tres elementos internos esenciales: el <strong>discernimiento</strong> (madurez y aptitud mental para comprender el alcance del acto), la <strong>intención</strong> (propósito consciente de realizar esa acción específica) y la <strong>libertad</strong> (obrar sin coacción física ni amenazas externas ilegítimas)."
            ],
            cuadro: {
              columnas: ["Concepto / Elemento", "Definición Técnica y Precisión Conceptual", "Límite o Consecuencia Práctica"],
              filas: [
                ["Libertad", "Facultad de autodeterminación consciente entre diversas opciones de conducta.", "Termina donde comienzan las leyes vigentes y los derechos de las demás personas (Art. 19 C.N.)."],
                ["Responsabilidad", "Deber ético y jurídico de responder, dar cuenta y asumir los efectos del propio obrar.", "Implica afrontar las consecuencias académicas, sociales o legales y reparar daños."],
                ["Requisitos del Acto Voluntario (Art. 260 CCyCN)", "1) Discernimiento (comprender), 2) Intención (querer hacerlo) y 3) Libertad (actuar sin coacción).", "Reunidos los tres requisitos, el sujeto responde plenamente por los resultados de su acción."],
                ["Libertinaje", "Conducta abusiva e irreflexiva que ignora las normas de convivencia y daña a terceros.", "Quebranta la paz comunitaria y acarrea sanciones disciplinarias o jurídicas."]
              ]
            },
            caso: {
              titulo: "Administración del tiempo, redes sociales y convivencia barrial",
              relato: "Lucas, alumno de 3.° año, tiene el fin de semana libre antes de una entrega obligatoria del lunes. Ejerciendo su libertad, decide pasar toda la tarde del domingo jugando en línea y escuchando música a volumen máximo en el patio de su casa hasta la medianoche, impidiendo el descanso de su vecino que debe trabajar temprano. El lunes por la mañana no presenta el trabajo práctico en el colegio y se queja diciendo que el profesor es injusto al desaprobarlo, y además se molesta porque su vecino reclamó a su familia por los ruidos molestos.",
              preguntaGuia: "¿En qué momento Lucas ejerció su libertad personal, cuándo incurrió en una conducta abusiva frente a terceros y qué responsabilidades pretende evadir?"
            },
            actividades: [
              "<strong>Fundamentación Teórica:</strong> Explicá con precisión qué significa la afirmación <em>'La responsabilidad es la otra cara inseparable de la moneda de la libertad'</em> y detallá los tres requisitos del acto voluntario (discernimiento, intención y libertad).",
              "<strong>Análisis Crítico de Caso:</strong> Evaluá la situación de Lucas diferenciando su decisión académica individual (administración del tiempo de estudio) de su conducta hacia el vecino (vulneración del derecho al descanso), indicando cómo debe responder en cada ámbito.",
              "<strong>Verificación de Comprensión Aplicada:</strong> Describí un ejemplo real de tu vida cotidiana como adolescente de 15 años (en el estudio, en las redes sociales o en la vía pública) donde ejerzas tu libertad de manera consciente y enumerá las responsabilidades que asumís en esa elección."
            ]
          },
          {
            id: "c4",
            numero: "Clase 4",
            titulo: "El Acto Moral: Intención, Medios y Fines",
            desarrollada: true,
            normativa: "Estructura Analítica de la Acción Moral • Deontología y Licitud de los Medios",
            teoria: [
              "No todas las acciones humanas revisten el mismo carácter ante la ética: los reflejos biológicos son involuntarios, pero ayudar a un par, decir la verdad o engañar son conductas deliberadas. Denominamos <strong>acto moral</strong> (acción consciente, libre y voluntaria ejecutada por una persona que es susceptible de valoración ética según parámetros de justicia y rectitud) a todo obrar humano que afecta la convivencia.",
              "Para evaluar con rigor un acto moral, desglosamos su <strong>estructura analítica tripartita</strong> (los tres componentes esenciales de la acción): en primer lugar, la <strong>intención</strong> (el fin interno y motivo subjetivo que impulsa al sujeto a obrar, es decir, <em>para qué</em> lo hace); en segundo lugar, los <strong>medios</strong> (los instrumentos, procedimientos y recursos empleados para lograrlo, es decir, <em>cómo</em> lo hace); y en tercer lugar, el <strong>fin objetivo o consecuencia</strong> (el resultado concreto producido en la realidad social, es decir, <em>qué efecto</em> causó).",
              "El principio rector de la ética establece que <strong>la rectitud de la intención no convalida el empleo de medios éticamente reprobables</strong> (en términos sencillos, un buen propósito jamás justifica utilizar métodos ilegales, violentos o fraudulentos). Para que un acto sea moralmente íntegro, tanto la intención como los medios y el resultado deben respetar la dignidad humana."
            ],
            cuadro: {
              columnas: ["Componente del Acto Moral", "Definición Técnica y Conceptual", "Pregunta Clave para el Análisis Ético"],
              filas: [
                ["1. Intención (Motivo Subjetivo)", "Propósito interno y deliberado que orienta la voluntad del sujeto antes de actuar.", "¿Qué buscaba lograr internamente la persona al decidir obrar?"],
                ["2. Medios (Instrumentos y Vías)", "Procedimientos, herramientas o métodos prácticos elegidos para concretar el propósito.", "¿Los recursos utilizados fueron lícitos, pacíficos y honestos, o vulneraron normas y derechos?"],
                ["3. Fin Objetivo (Consecuencia)", "Resultado efectivo y verificable que la acción produce en el entorno comunitario.", "¿Qué efectos reales generó el acto sobre terceras personas y la institución?"],
                ["Regla de Integridad Ética", "Invalidez del axioma 'el fin justifica los medios': un fin loable no legitima un medio ilícito.", "¿Son éticamente válidos los tres elementos (intención, medio y fin) al mismo tiempo?"]
              ]
            },
            caso: {
              titulo: "La autorización falsificada para el certamen escolar",
              relato: "Dos estudiantes de 3.° año prepararon durante semanas un proyecto de ciencias para representar a su escuela en un certamen intercolegial en Posadas. El día del viaje, uno de ellos advierte que olvidó hacer firmar la autorización obligatoria por sus padres, quienes se encuentran trabajando en una zona rural sin señal telefónica. Con el propósito de que su amigo no quede afuera del concurso ni pierda todo el esfuerzo del año, su compañero toma una lapicera e imita la firma del padre en la planilla oficial antes de entregarla al preceptor.",
              preguntaGuia: "¿Alcanza la buena intención solidaria del compañero para que el acto de falsificar una firma oficial sea éticamente válido?"
            },
            actividades: [
              "<strong>Desglose Estructural:</strong> Describí analíticamente los tres elementos constitutivos del <em>acto moral</em> (intención, medios y fin objetivo) y fundamentá racionalmente por qué el fin nunca justifica la utilización de medios ilegítimos.",
              "<strong>Evaluación Ética de Caso:</strong> Analizá el caso del estudiante que falsifica la autorización institucional para ayudar a su compañero, identificando por separado cuál fue su <em>intención</em>, cuál fue el <em>medio empleado</em> y cuáles son las <em>consecuencias institucionales y legales</em> de ese acto.",
              "<strong>Resolución Alternativa de Conflictos:</strong> Evaluá este segundo supuesto del cuadernillo: <em>'Un estudiante quiere defender a un amigo que está siendo agredido verbalmente (intención) y para lograrlo golpea físicamente al agresor dejándolo herido (medio y fin)'</em>. Explicá por qué el medio elegido invalida el acto y qué medio pacífico e institucional debió utilizar."
            ]
          }
        ]
      },
      {
        id: "u2",
        numero: "Unidad 2",
        titulo: "Dignidad y Derechos Humanos",
        activa: false,
        clases: [
          {
            id: "c5",
            numero: "Clase 5",
            titulo: "La Persona Humana como Fin en Sí Mismo",
            desarrollada: true,
            normativa: "Imperativo Categórico Kantiano • Art. 51 del Código Civil y Comercial de la Nación (Inviolabilidad de la Persona) • Art. 1 DUDH",
            teoria: [
              "Inspirado en la formulación del <strong>imperativo categórico kantiano</strong> (principio ético enunciado por el filósofo Immanuel Kant que exige obrar siempre tratando a la humanidad, tanto en la propia persona como en la de cualquier otro, siempre como un fin y nunca meramente como un medio), el principio de <strong>dignidad humana</strong> consagra que todo individuo posee un <strong>valor intrínseco, incondicionado e inestimable</strong> (una valía absoluta por el solo hecho de ser persona, que no depende de su nivel económico, utilidad ni rendimiento).",
              "Para comprender este fundamento, distinguimos filosóficamente dos realidades: aquello que tiene <strong>precio</strong> (las cosas u objetos materiales, que cumplen una función instrumental, se tasan en dinero y pueden intercambiarse o sustituirse por un equivalente) y aquello que tiene <strong>dignidad</strong> (las personas humanas, que son únicas, irremplazables y se encuentran por encima de toda cotización mercantil).",
              "De aquí emana la <strong>proscripción de instrumentalización o cosificación</strong> (prohibición ética y jurídica —plasmada en el artículo 51 del Código Civil y Comercial de la Nación sobre la inviolabilidad de la persona humana— de degradar a un semejante a la condición de simple objeto, herramienta o recurso utilitario para alcanzar metas ajenas). A las cosas se las usa; a las personas se las respeta como fines en sí mismas."
            ],
            cuadro: {
              columnas: ["Criterio Filosófico y Jurídico", "Lo que tiene PRECIO (Las Cosas)", "Lo que tiene DIGNIDAD (Las Personas)"],
              filas: [
                ["Naturaleza del Valor", "Valor extrínseco, relativo y medible en dinero según su utilidad o demanda.", "Valor intrínseco, absoluto e incondicionado que pertenece a todo ser humano."],
                ["Posibilidad de Sustitución", "Intercambiable y reemplazable por otro objeto de idéntica función o costo.", "Única, singular e irremplazable: ninguna persona equivale a una mercancía."],
                ["Rol en la Acción Humana", "Opera como medio, instrumento o herramienta para obtener un resultado.", "Constituye un fin en sí misma: jamás puede ser tratada como mero engranaje."],
                ["Deber Ético y Legal", "Uso, administración, compraventa o reemplazo material.", "Respeto irrestricto, inviolabilidad (Art. 51 CCyCN) y tutela de sus derechos."]
              ]
            },
            caso: {
              titulo: "Vínculos por conveniencia y cosificación en el grupo escolar",
              relato: "Al comenzar el trimestre en 3.° año, ingresa al curso un estudiante nuevo que se destaca por su habilidad para resolver trabajos prácticos de matemática e informática. Un grupo de compañeros decide integrarlo a su equipo e invitarlo a juntarse por la tarde, pero en su grupo privado de WhatsApp comentan: 'Seamos amables con él hasta que nos pase todos los trabajos resueltos del trimestre; después que se arregle solo'. Cuando termina la entrega de notas, dejan de hablarle y lo excluyen de las actividades.",
              preguntaGuia: "¿Por qué la conducta del grupo quebranta el imperativo kantiano al tratar al compañero como un mero medio en lugar de reconocerlo como un fin en sí mismo?"
            },
            actividades: [
              "<strong>Síntesis Comparativa:</strong> Elaborá con precisión conceptual la distinción filosófica entre los conceptos de <em>'Precio'</em> (valor relativo e instrumental de las cosas) y <em>'Dignidad'</em> (valor intrínseco e incondicionado de las personas).",
              "<strong>Evaluación de Situaciones (Fin vs. Medio):</strong> Analizá el caso del estudiante nuevo en el curso y explicá en qué consiste la <em>instrumentalización o cosificación</em> del semejante. Luego, comparalo con la actitud de ayudar a un compañero sin exigir beneficios materiales ni favores a cambio.",
              "<strong>Fundamentación Constitucional:</strong> Argumentá por qué el reconocimiento de la persona humana como un <em>fin en sí misma</em> constituye la piedra basal de todos los Derechos Humanos y del Estado Constitucional de Derecho."
            ]
          },
          {
            id: "c6",
            numero: "Clase 6",
            titulo: "Historia y Características de los Derechos Humanos",
            desarrollada: true,
            normativa: "Declaración Universal de los Derechos Humanos (ONU, 10 de diciembre de 1948) • Art. 1 DUDH",
            teoria: [
              "Tras las aberraciones cometidas durante la Segunda Guerra Mundial y el Holocausto, la comunidad internacional comprendió que la dignidad humana no podía quedar desprotegida frente a los abusos de poder y proclamó el 10 de diciembre de 1948 la <strong>Declaración Universal de los Derechos Humanos (DUDH)</strong> ante la Organización de las Naciones Unidas (ONU), cuyo artículo 1 establece que todos los seres humanos nacen libres e iguales en dignidad y derechos.",
              "Los <strong>Derechos Humanos</strong> (conjunto de prerrogativas, facultades y libertades fundamentales inherentes a la naturaleza humana, es decir, derechos que pertenecen a cada individuo por el solo hecho de ser persona y que no son una concesión ni un regalo de los gobernantes, sino un límite infranqueable al poder estatal) constituyen el piso ético y jurídico innegociable de toda sociedad democrática.",
              "Sus cuatro <strong>caracteres dogmáticos estructurales</strong> son: 1) <strong>Universalidad</strong> (corresponden a todas las personas del mundo sin distinción de etnia, género, nacionalidad, religión o condición social); 2) <strong>Inalienabilidad</strong> (son irrenunciables e intransferibles: nadie puede venderlos ni firmar un contrato válido para ceder su libertad o integridad); 3) <strong>Imprescriptibilidad</strong> (tienen vigencia perpetua, no caducan con la edad ni el tiempo, por lo que los crímenes de lesa humanidad no prescriben jamás); y 4) <strong>Indivisibilidad e Interdependencia</strong> (forman un sistema integral donde no se puede garantizar un derecho —como educarse— si se priva de otros esenciales como la salud y la alimentación)."
            ],
            cuadro: {
              columnas: ["Característica Estructural", "Definición Técnica y Sencilla", "Prohibición Legal Terminante", "Ejemplo Cotidiano (15 años)"],
              filas: [
                ["1. Universalidad", "Titularidad extensiva a todo el género humano sin exclusiones.", "Prohíbe discriminar por origen étnico, nacionalidad, género, credo o recursos económicos.", "Tanto un joven en Oberá como un migrante gozan de idéntico derecho a la salud y a la educación."],
                ["2. Inalienabilidad", "Imposibilidad jurídica de enajenar, vender, transferir o renunciar al derecho.", "Anula de pleno derecho cualquier pacto de servidumbre o renuncia a derechos básicos.", "Si un comercio hace firmar a un adolescente que 'renuncia a su descanso', ese papel es nulo."],
                ["3. Imprescriptibilidad", "Vigencia perpetua: no se extinguen ni se pierden por el paso de los años.", "Impide que el transcurso del tiempo deje impunes delitos de lesa humanidad.", "Los derechos se mantienen toda la vida y los crímenes de Estado se juzgan décadas después."],
                ["4. Indivisibilidad", "Unidad interdependiente: todos los derechos poseen igual jerarquía.", "Prohíbe reconocer un derecho formalmente negando las condiciones materiales de otro.", "Para ejercer el derecho a estudiar, el alumno requiere nutrición, salud y vida libre de violencia."]
              ]
            },
            caso: {
              titulo: "Condicionamiento económico e intento de renuncia de derechos",
              relato: "Se presentan dos situaciones en nuestra comunidad: En el Caso A, una institución educativa pretende impedir la inscripción de una alumna de 3.° año porque su familia atraviesa dificultades económicas y no puede abonar el bono de cooperadora escolar. En el Caso B, un comercio local contrata durante el verano a un joven de 16 años y le exige firmar una nota privada donde el adolescente declara 'renunciar por propia voluntad a sus francos semanales y a las medidas de seguridad laboral' a cambio de una propina extra.",
              preguntaGuia: "¿Qué caracteres estructurales de los Derechos Humanos invalidan la exclusión escolar en el Caso A y anulan la nota firmada en el Caso B?"
            },
            actividades: [
              "<strong>Contexto Histórico y Naturaleza Jurídica:</strong> Explicá qué acontecimientos históricos mundiales motivaron la proclamación de la <em>Declaración Universal de los Derechos Humanos en 1948</em> y fundamentá por qué estos derechos son <em>inherentes</em> a la persona y no una concesión de los gobiernos.",
              "<strong>Análisis Técnico de Caracteres:</strong> Definí analíticamente las notas de <em>Inalienabilidad</em>, <em>Imprescriptibilidad</em> e <em>Indivisibilidad</em>, y resolvé los Casos A y B del relato explicando por qué la renuncia firmada por el joven es jurídicamente nula.",
              "<strong>Compromiso Ciudadano Escolar:</strong> Redactá dos pautas concretas de convivencia para implementar en tu curso o en los grupos digitales estudiantiles que garanticen el principio de <em>Universalidad y No Discriminación</em> frente a diferencias económicas, de origen o de opinión."
            ]
          },
          {
            id: "c7",
            numero: "Clase 7",
            titulo: "Matriz Constitucional y Tratados Internacionales",
            desarrollada: true,
            normativa: "Arts. 31 y 75 inciso 22 de la Constitución de la Nación Argentina (Reforma Constitucional de 1994)",
            teoria: [
              "En un Estado federal como la República Argentina coexisten normas nacionales, provinciales (como las leyes de Misiones), ordenanzas municipales y reglamentos escolares. Para garantizar la coherencia del sistema rige el <strong>principio de supremacía constitucional</strong> (consagrado en el artículo 31 de la Constitución Nacional, según el cual todas las leyes y actos inferiores deben subordinarse a la Constitución sin contradecirla).",
              "Con la reforma constitucional de 1994, el <strong>artículo 75 inciso 22 de la Constitución Nacional</strong> otorgó <strong>jerarquía constitucional</strong> (el máximo rango jurídico del país, compartiendo la cima con la Carta Magna) a los principales Tratados Internacionales de Derechos Humanos, entre ellos la Declaración Universal de 1948, el Pacto de San José de Costa Rica y la Convención sobre los Derechos del Niño.",
              "Esta cúspide de la <strong>Pirámide Jurídica de Kelsen</strong> (representación escalonada de la jerarquía de las leyes) conforma el <strong>Bloque de Constitucionalidad Federal</strong> (la unión suprema de la Constitución Nacional y los Tratados de DD.HH. del Art. 75 inc. 22). Cualquier norma local, provincial o nacional que lesione este bloque deviene inconstitucional e inaplicable."
            ],
            cuadro: {
              columnas: ["Nivel de la Pirámide Jurídica Argentina", "Normas que Integran el Escalón", "Alcance y Subordinación Normativa"],
              filas: [
                ["Nivel 1 (Cúspide Suprema): Bloque de Constitucionalidad", "Constitución Nacional + Tratados Internacionales de DD.HH. con jerarquía constitucional (Art. 75 inc. 22 C.N.).", "Vértice supremo del ordenamiento argentino: ninguna norma del país puede vulnerar sus garantías."],
                ["Nivel 2: Otros Tratados y Leyes Nacionales", "Demás tratados internacionales y Leyes Nacionales sancionadas por el Congreso (ej. CCyCN, Ley 26.061).", "Subordinadas al Nivel 1; prevalecen sobre las normativas provinciales y municipales."],
                ["Nivel 3: Ordenamiento Provincial", "Constitución de la Provincia de Misiones y Leyes Provinciales de la Cámara de Representantes.", "Rigen en el ámbito provincial respetando la Constitución Nacional y las leyes federales."],
                ["Nivel 4 (Base): Normativa Municipal y Escolar", "Ordenanzas de los Concejos Deliberantes (ej. Oberá), resoluciones y reglamentos escolares.", "Deben adecuarse a todos los escalones superiores; si restringen derechos humanos, son nulas."]
              ]
            },
            caso: {
              titulo: "Choque entre un reglamento local y la Convención sobre los Derechos del Niño",
              relato: "En un municipio de nuestra provincia se dicta una disposición local que prohíbe a los adolescentes menores de 18 años reunirse pacíficamente en plazas públicas después de las 19:00 horas o presentar peticiones colectivas ante las autoridades municipales, y paralelamente una escuela pretende aplicar un reglamento interno que impide a los alumnos ser escuchados antes de aplicarles una sanción disciplinaria. Los estudiantes plantean que ambas medidas violan la Constitución Nacional y la Convención sobre los Derechos del Niño (Art. 75 inc. 22 C.N.).",
              preguntaGuia: "Aplicando la Pirámide Jurídica de los artículos 31 y 75 inciso 22 de la Constitución Nacional, ¿qué validez tienen esa disposición municipal y ese reglamento interno?"
            },
            actividades: [
              "<strong>Esquematización Normativa:</strong> Dibujá o estructurá en tu carpeta la <em>Pirámide Jurídica Argentina</em> en sus 4 niveles conforme a los artículos 31 y 75 inciso 22 de la Constitución Nacional, explicando qué es el <em>Bloque de Constitucionalidad Federal</em>.",
              "<strong>Ordenamiento Jerárquico Práctico:</strong> Ordená de mayor a menor jerarquía (del Nivel 1 al Nivel 4) las siguientes normas: a) <em>Ordenanza de tránsito del Concejo Deliberante de Oberá</em>; b) <em>Ley Provincial de Educación de Misiones</em>; c) <em>Convención Americana sobre Derechos Humanos (Art. 75 inc. 22 C.N.)</em>; d) <em>Código Civil y Comercial de la Nación</em>.",
              "<strong>Resolución de Inconstitucionalidad:</strong> Analizá el caso del municipio y del reglamento escolar que restringen el derecho de reunión pacífica y el derecho a ser oído, explicando por qué esas normas inferiores son inconstitucionales e inaplicables."
            ]
          },
          {
            id: "c8",
            numero: "Clase 8",
            titulo: "Vulneración de Derechos y Garantías Constitucionales",
            desarrollada: true,
            normativa: "Arts. 18 y 43 de la Constitución de la Nación Argentina (Acción de Amparo, Habeas Data y Habeas Corpus)",
            teoria: [
              "Mientras los derechos son las facultades reconocidas a cada ciudadano, las <strong>garantías constitucionales</strong> (mecanismos procesales jurisdiccionales rápidos y expeditos que la Constitución otorga a las personas para acudir ante el Poder Judicial y frenar de inmediato un abuso o vulneración de derechos cometida por autoridades públicas o por particulares) constituyen el escudo práctico que asegura su cumplimiento efectivo.",
              "El <strong>artículo 43 de la Constitución Nacional</strong> consagra tres garantías fundamentales: en primer término, el <strong>Habeas Corpus</strong> (remedio judicial urgente que protege la libertad física, ambulatoria y la integridad corporal frente a detenciones arbitrarias sin orden escrita de juez competente, amenazas de arresto ilegal o agravamiento ilegítimo de las condiciones de detención).",
              "En segundo término, el <strong>Habeas Data</strong> (garantía que tutela la intimidad, el honor y la autodeterminación informativa, facultando a toda persona a conocer los datos propios registrados en bancos públicos o privados y exigir su rectificación, supresión o confidencialidad). En tercer término, la <strong>Acción de Amparo</strong> (vía judicial rápida contra todo acto u omisión manifiestamente ilegal o arbitrario que lesione de forma actual o inminente cualquier otro derecho constitucional —como la salud, la educación o el ambiente— no alcanzado por el Habeas Corpus)."
            ],
            cuadro: {
              columnas: ["Garantía Constitucional (Art. 43 C.N.)", "Derecho Fundamental que Tutela", "Presupuesto Fáctico (Cuándo procede)", "Ejemplo de Aplicación Concreta"],
              filas: [
                ["Habeas Corpus", "Libertad física, ambulatoria (de circular) e integridad psicofísica.", "Ante detención arbitraria sin orden judicial, amenaza ilegal de arresto o malos tratos en encierro.", "Un joven es retenido e incomunicado en una dependencia sin causa legal ni orden de un juez."],
                ["Habeas Data", "Honor, intimidad, privacidad y veracidad de los datos personales.", "Cuando un registro público o base privada almacena información falsa, errónea o discriminatoria.", "Una base comercial publica por error que una persona es deudora, impidiéndole conseguir empleo."],
                ["Acción de Amparo", "Demás derechos constitucionales (salud, educación, ambiente sano, trabajo).", "Frente a un acto u omisión manifiestamente arbitrario o ilegal que requiere solución urgente.", "Una obra social niega injustificadamente una cirugía o medicación vital urgente a un estudiante."]
              ]
            },
            caso: {
              titulo: "Tres emergencias ciudadanas ante los tribunales de Misiones",
              relato: "En una misma semana se presentan tres situaciones urgentes en la ciudad: 1) A la salida de un recital juvenil, un joven de 17 años es retenido por efectivos sin que exista delito ni orden judicial y permanece incomunicado durante horas; 2) Una empresa privada de informes crediticios e internet difunde datos falsos sobre la salud y supuestas deudas de una trabajadora local, provocándole el rechazo en una búsqueda laboral; 3) Una familia reclama que la prestataria de salud le niega a su hijo de 15 años una cirugía oftalmológica urgente, corriendo riesgo de perder la vista si espera un juicio ordinario de varios años.",
              preguntaGuia: "¿Cuál de las tres garantías específicas del artículo 43 de la Constitución Nacional (Habeas Corpus, Habeas Data o Acción de Amparo) debe interponerse en cada una de las tres situaciones y por qué?"
            },
            actividades: [
              "<strong>Distinción Conceptual y Procesal:</strong> Explicá qué diferencia existe entre un <em>derecho constitucional</em> y una <em>garantía constitucional</em>, y distinguí con precisión técnica los presupuestos que diferencian al <em>Habeas Corpus</em> del <em>Habeas Data</em>.",
              "<strong>Dictamen de Asignación de Garantías:</strong> Resolvé las tres emergencias planteadas en el caso práctico (la detención arbitraria a la salida del recital, el registro informático falso y la negativa de cirugía urgente), fundamentando qué garantía del artículo 43 de la Constitución Nacional corresponde activar en cada inciso.",
              "<strong>Redacción de Caso Hipotético:</strong> Redactá un caso verosímil situado en nuestra provincia en el cual se vulnere el derecho a la educación o el derecho a un ambiente sano, y explicá cómo funcionaría una <em>Acción de Amparo</em> para restablecer el derecho lesionado."
            ]
          }
        ]
      },
      {
        id: "u3",
        numero: "Unidad 3",
        titulo: "Adolescencia e Identidad",
        activa: false,
        clases: [
          {
            id: "c9",
            numero: "Clase 9",
            titulo: "Construcción de la Identidad en la Adolescencia",
            desarrollada: true,
            normativa: "Psicología Evolutiva • Ley Nacional N.° 26.061 de Protección Integral de los Derechos de Niñas, Niños y Adolescentes",
            teoria: [
              "La <strong>identidad</strong> (constructo psicosocial dinámico, relacional y multidimensional mediante el cual cada sujeto configura progresivamente su subjetividad, su esquema corporal, su sistema de valores y su proyecto de vida en interacción con su comunidad) no es una estructura rígida ni biológicamente predeterminada, sino un proceso de construcción continua a lo largo de la existencia.",
              "Durante la adolescencia, el individuo transita una etapa decisiva de <strong>reelaboración simbólica y subjetiva</strong> (reorganización de la propia imagen, cuestionamiento reflexivo de los mandatos infantiles heterónomos y exploración activa de vocaciones, intereses culturales y convicciones éticas) orientada a cimentar su madurez e independencia.",
              "Este recorrido permite afianzar la <strong>singularidad personal</strong> (la afirmación de la propia autenticidad y del proyecto vital elegido libremente frente a las expectativas o estereotipos impuestos por el entorno sociocultural), amparada jurídicamente por la Ley Nacional N.° 26.061 bajo el principio de autonomía progresiva."
            ],
            cuadro: {
              columnas: ["Dimensión de Análisis", "Etapa Infantil (Mandatos Iniciales)", "Etapa Adolescente (
