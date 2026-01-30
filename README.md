[!DOCTYPE.html](https://github.com/user-attachments/files/24951186/DOCTYPE.html)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini-Test de Temperamentos - Basado en Grok</title>
    <style>
        body { font-family: Arial, sans-serif; max-width: 800px; margin: 0 auto; padding: 20px; background-color: #f4f4f4; }
        h1 { text-align: center; color: #333; }
        .question { margin-bottom: 20px; }
        .question label { display: block; margin: 5px 0; }
        button { display: block; margin: 20px auto; padding: 10px 20px; background-color: #007bff; color: white; border: none; cursor: pointer; }
        button:hover { background-color: #0056b3; }
        #result { margin-top: 30px; padding: 20px; background-color: white; border: 1px solid #ddd; border-radius: 5px; }
    </style>
</head>
<body>
    <h1>Mini-Test de los 4 Temperamentos</h1>
    <p>Basado en la teoría de Hipócrates y adaptado por Grok (xAI). Responde honestamente. Puedes elegir más de una opción por pregunta si te identificás con varias.</p>

    <form id="quizForm">
        <!-- Pregunta 1 -->
        <div class="question">
            <p>1. En una fiesta o reunión grande con gente nueva:</p>
            <label><input type="checkbox" name="q1" value="A"> A) Soy el que anima todo, hablo con todos, me divierto mucho y hago chistes.</label>
            <label><input type="checkbox" name="q1" value="B"> B) Tomo el control: organizo juegos, decido qué hacer, lidero el grupo.</label>
            <label><input type="checkbox" name="q1" value="C"> C) Me quedo más observando, converso en profundidad con 1-2 personas, o me voy temprano si me aburro.</label>
            <label><input type="checkbox" name="q1" value="D"> D) Estoy cómodo, escucho, ayudo si alguien necesita algo, pero no busco ser el centro.</label>
        </div>

        <!-- Pregunta 2 -->
        <div class="question">
            <p>2. Cuando hay un problema o emergencia repentina:</p>
            <label><input type="checkbox" name="q2" value="A"> A) Me emociono, actúo rápido por impulso, pero a veces me disperso.</label>
            <label><input type="checkbox" name="q2" value="B"> B) Tomo decisiones firmes y rápidas, digo qué hay que hacer y lo hago ya.</label>
            <label><input type="checkbox" name="q2" value="C"> C) Pienso mucho en todos los riesgos y detalles antes de actuar, me preocupo.</label>
            <label><input type="checkbox" name="q2" value="D"> D) Mantengo la calma total, ayudo paso a paso sin alterarme.</label>
        </div>

        <!-- Pregunta 3 -->
        <div class="question">
            <p>3. Cómo eres con las metas o tareas:</p>
            <label><input type="checkbox" name="q3" value="A"> A) Empiezo con mucha energía y entusiasmo, pero a veces dejo cosas a medias.</label>
            <label><input type="checkbox" name="q3" value="B"> B) Voy a full hasta terminar, odio fallar, soy muy competitivo.</label>
            <label><input type="checkbox" name="q3" value="C"> C) Planifico todo al detalle, quiero que salga perfecto, me cuesta empezar si no está bien.</label>
            <label><input type="checkbox" name="q3" value="D"> D) Hago lo que hay que hacer de forma constante y sin drama, prefiero rutina estable.</label>
        </div>

        <!-- Pregunta 4 -->
        <div class="question">
            <p>4. En el trabajo o estudios, qué te motiva más:</p>
            <label><input type="checkbox" name="q4" value="A"> A) Estar con gente, pasarla bien, que me reconozcan o elogien.</label>
            <label><input type="checkbox" name="q4" value="B"> B) Lograr resultados, ganar, tener poder o éxito visible.</label>
            <label><input type="checkbox" name="q4" value="C"> C) Hacerlo bien, aprender profundo, que sea de calidad o significativo.</label>
            <label><input type="checkbox" name="q4" value="D"> D) Paz, armonía, ayudar a otros, evitar conflictos.</label>
        </div>

        <!-- Pregunta 5 -->
        <div class="question">
            <p>5. Cómo manejas el estrés o enojo:</p>
            <label><input type="checkbox" name="q5" value="A"> A) Me enojo rápido pero se me pasa pronto, hablo o río para desahogarme.</label>
            <label><input type="checkbox" name="q5" value="B"> B) Exploto fuerte si me provocan, pero controlo si vale la pena.</label>
            <label><input type="checkbox" name="q5" value="C"> C) Me guardo todo, me pongo triste o rumio mucho tiempo.</label>
            <label><input type="checkbox" name="q5" value="D"> D) Casi no exploto, lo proceso internamente y sigo tranquilo.</label>
        </div>

        <!-- Pregunta 6 -->
        <div class="question">
            <p>6. En relaciones (amigos, pareja, familia):</p>
            <label><input type="checkbox" name="q6" value="A"> A) Muy expresivo, cariñoso, busco diversión y atención constante.</label>
            <label><input type="checkbox" name="q6" value="B"> B) Directo, protector, exijo lealtad y respeto.</label>
            <label><input type="checkbox" name="q6" value="C"> C) Leal y profundo, pero reservado, sensible a críticas.</label>
            <label><input type="checkbox" name="q6" value="D"> D) Paciente, comprensivo, buen escucha, evito peleas.</label>
        </div>

        <!-- Pregunta 7 -->
        <div class="question">
            <p>7. Qué te describe mejor en una palabra clave:</p>
            <label><input type="checkbox" name="q7" value="A"> A) Entusiasta / Sociable</label>
            <label><input type="checkbox" name="q7" value="B"> B) Decidido / Líder</label>
            <label><input type="checkbox" name="q7" value="C"> C) Perfeccionista / Analítico</label>
            <label><input type="checkbox" name="q7" value="D"> D) Tranquilo / Paciente</label>
        </div>

        <!-- Pregunta 8 -->
        <div class="question">
            <p>8. Si tuvieras que elegir un rol en un equipo:</p>
            <label><input type="checkbox" name="q8" value="A"> A) El motivador o el que pone buena onda.</label>
            <label><input type="checkbox" name="q8" value="B"> B) El jefe o el que toma decisiones.</label>
            <label><input type="checkbox" name="q8" value="C"> C) El que planea y chequea detalles.</label>
            <label><input type="checkbox" name="q8" value="D"> D) El que apoya y mantiene todo en equilibrio.</label>
        </div>

        <button type="button" onclick="calculateResult()">Calcular mi Temperamento</button>
    </form>

    <div id="result" style="display: none;"></div>

    <script>
        function calculateResult() {
            const scores = { A: 0, B: 0, C: 0, D: 0 };
            const questions = document.querySelectorAll('.question');
            questions.forEach(q => {
                const checkboxes = q.querySelectorAll('input[type="checkbox"]:checked');
                checkboxes.forEach(cb => {
                    scores[cb.value]++;
                });
            });

            // Encontrar el máximo y secundarios
            const maxScore = Math.max(scores.A, scores.B, scores.C, scores.D);
            const primary = Object.keys(scores).find(key => scores[key] === maxScore);
            const types = { A: 'Sanguíneo', B: 'Colérico', C: 'Melancólico', D: 'Flemático' };

            // Secundarios: cualquiera con score >= maxScore - 1 (o ajustá si querés)
            let secondaries = [];
            Object.keys(scores).forEach(key => {
                if (key !== primary && scores[key] >= maxScore - 1) {
                    secondaries.push(types[key]);
                }
            });
            const secondaryText = secondaries.length > 0 ? `con toques de ${secondaries.join(' + ')}` : 'puro';

            // Definiciones basadas en Grok
            const descriptions = {
                A: 'Extrovertido, sociable, entusiasta. Sos el alma de la fiesta, optimista y cariñoso, pero a veces impulsivo o desorganizado.',
                B: 'Líder nato, decidido, ambicioso. Tomás control, sos directo y orientado a metas, pero podés ser impaciente o dominante.',
                C: 'Analítico, perfeccionista, profundo. Sos reflexivo, creativo y detallista, pero a veces pesimista o autocrítico.',
                D: 'Tranquilo, paciente, diplomático. Sos equilibrado, leal y buen escucha, pero a veces pasivo o indeciso.'
            };

            // Fortalezas y debilidades basadas en Grok
            const strengths = {
                A: 'Fácil conexión con gente, energía positiva, adaptable.',
                B: 'Decisión rápida, liderazgo, resultados concretos.',
                C: 'Precisión, profundidad, creatividad.',
                D: 'Calma bajo presión, empatía, estabilidad.'
            };
            const weaknesses = {
                A: 'Dispersión, superficialidad en tareas largas.',
                B: 'Explosividad, dominancia excesiva.',
                C: 'Sobrepensar, tendencia a la tristeza.',
                D: 'Pasividad, lentitud en cambios.'
            };

            // Encaje con policía (como ejemplo, basado en nuestra charla)
            let policeFit = '';
            if (primary === 'D') {
                policeFit = 'Excelente match: calma y resiliencia para emergencias.';
            } else if (primary === 'B') {
                policeFit = 'Bueno para liderazgo, pero controlá impulsos.';
            } else {
                policeFit = 'Posible, pero usá tus secundarios para equilibrar.';
            }

            // Mostrar resultado
            const resultDiv = document.getElementById('result');
            resultDiv.innerHTML = `
                <h2>Tu Temperamento Principal: ${types[primary]} (${secondaryText})</h2>
                <p>${descriptions[primary]}</p>
                <h3>Fortalezas:</h3><p>${strengths[primary]}</p>
                <h3>Debilidades:</h3><p>${weaknesses[primary]}</p>
                <h3>Ejemplo de Encaje Profesional (Oficial de Policía):</h3><p>${policeFit}</p>
                <p>Puntajes: Sanguíneo: ${scores.A}, Colérico: ${scores.B}, Melancólico: ${scores.C}, Flemático: ${scores.D}</p>
                <p>Basado en análisis de Grok (xAI) - ¡Compartí con amigos!</p>
            `;
            resultDiv.style.display = 'block';
        }
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini-Test de Temperamentos - Grok Edition</title>
    <style>
        :root {
            --bg: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            --text: #e0e0ff;
            --accent: #00f0ff; /* Cyan neón suave */
            --accent-glow: #00f0ff33;
            --card: rgba(30, 30, 60, 0.7);
            --button: #6a0dad;
            --button-hover: #9d4edd;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 20px;
            min-height: 100vh;
            background-attachment: fixed;
        }

        h1 {
            text-align: center;
            color: var(--accent);
            text-shadow: 0 0 15px var(--accent-glow);
            margin-bottom: 10px;
            animation: fadeIn 1.5s ease-out;
        }

        p.intro {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 30px;
            opacity: 0.9;
        }

        .question {
            background: var(--card);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 25px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(0, 240, 255, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .question:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 40px rgba(0, 240, 255, 0.15);
        }

        label {
            display: block;
            margin: 12px 0;
            padding: 12px;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.05);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        label:hover {
            background: rgba(0, 240, 255, 0.1);
            transform: translateX(5px);
        }

        input[type="checkbox"]:checked + span {
            color: var(--accent);
            font-weight: bold;
        }

        /* Para que el label muestre el texto correctamente */
        label span { display: inline; }

        button {
            display: block;
            margin: 30px auto;
            padding: 15px 40px;
            font-size: 1.2em;
            background: var(--button);
            color: white;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 0 20px rgba(106, 13, 173, 0.5);
            transition: all 0.4s ease;
        }

        button:hover {
            background: var(--button-hover);
            transform: scale(1.08);
            box-shadow: 0 0 30px rgba(157, 78, 221, 0.7);
        }

        #result {
            margin-top: 40px;
            padding: 30px;
            background: var(--card);
            border-radius: 16px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.6);
            border: 1px solid rgba(0, 240, 255, 0.15);
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 1s ease, transform 1s ease;
        }

        #result.show {
            opacity: 1;
            transform: translateY(0);
        }

        #result h2 {
            color: var(--accent);
            text-shadow: 0 0 10px var(--accent-glow);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }

        .error-shake {
            animation: shake 0.5s ease;
        }
    </style>
</head>
<body>
    <h1>Mini-Test de los 4 Temperamentos</h1>
    <p class="intro">Basado en la teoría clásica y adaptado por Grok (xAI). Responde lo que más te represente. Puedes seleccionar varias opciones por pregunta.</p>

    <form id="quizForm">
        <!-- Las mismas 8 preguntas que antes, pero con <span> para estilizar mejor -->
        <div class="question">
            <p>1. En una fiesta o reunión grande con gente nueva:</p>
            <label><input type="checkbox" name="q1" value="A"><span> A) Soy el que anima todo, hablo con todos, me divierto mucho y hago chistes.</span></label>
            <label><input type="checkbox" name="q1" value="B"><span> B) Tomo el control: organizo juegos, decido qué hacer, lidero el grupo.</span></label>
            <label><input type="checkbox" name="q1" value="C"><span> C) Me quedo más observando, converso en profundidad con 1-2 personas, o me voy temprano si me aburro.</span></label>
            <label><input type="checkbox" name="q1" value="D"><span> D) Estoy cómodo, escucho, ayudo si alguien necesita algo, pero no busco ser el centro.</span></label>
        </div>

        <!-- Repite para q2 a q8 igual que en tu versión anterior, solo cambia <label> a tener <input> y <span>texto</span> -->
        <!-- Para no alargar demasiado, asumo que copiás el resto de preguntas igual, solo agregando <span> alrededor del texto -->

        <!-- ... (pega las otras 7 preguntas aquí con el mismo formato) ... -->

        <button type="button" onclick="calculateResult()">Calcular mi Temperamento</button>
    </form>

    <div id="result"></div>

    <script>
        function calculateResult() {
            const scores = { A: 0, B: 0, C: 0, D: 0 };
            let answered = false;

            document.querySelectorAll('.question input[type="checkbox"]').forEach(cb => {
                if (cb.checked) {
                    scores[cb.value]++;
                    answered = true;
                }
            });

            if (!answered) {
                document.querySelector('button').classList.add('error-shake');
                setTimeout(() => document.querySelector('button').classList.remove('error-shake'), 600);
                alert('¡Elegí al menos una opción!');
                return;
            }

            const maxScore = Math.max(scores.A, scores.B, scores.C, scores.D);
            const primaryKey = Object.keys(scores).find(k => scores[k] === maxScore);
            const types = { A: 'Sanguíneo', B: 'Colérico', C: 'Melancólico', D: 'Flemático' };

            let secondaries = [];
            Object.keys(scores).forEach(k => {
                if (k !== primaryKey && scores[k] >= maxScore - 1) secondaries.push(types[k]);
            });
            const secondaryText = secondaries.length ? `con toques de ${secondaries.join(' + ')}` : 'puro';

            // Resto de la lógica de descripciones, fortalezas, etc. (copiá del código anterior)
            // Para no repetir, usa la misma que tenías en calculateResult()

            const resultDiv = document.getElementById('result');
            resultDiv.innerHTML = `...`;  // pega tu HTML de resultado aquí
            resultDiv.classList.add('show');
            resultDiv.scrollIntoView({ behavior: 'smooth' });
        }
    </script>
</body>
</html>
