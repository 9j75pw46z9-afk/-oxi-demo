# -oxi-demo
    asistente IA Oxymar
<!doctype html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#0b1b2b">
  <title>Oxymar IA — Demo</title>
  <link rel="stylesheet" href="styles.css">
</head>

<body>

  <div class="app">

    <!-- BARRA LATERAL -->
    <aside class="sidebar" id="sidebar">

      <div class="brand">
        <div class="brand-mark">O</div>
        <div>
          <strong>Oxymar</strong>
          <span>Asistente IA</span>
        </div>
      </div>

      <button class="new-chat" id="newChat">
        ＋ Nueva conversación
      </button>

      <div class="side-label">
        Accesos rápidos
      </div>

      <button class="quick" data-message="¿Qué servicios ofrece Oxymar?">
        Información
      </button>

      <button class="quick" data-message="Quiero solicitar un presupuesto.">
        Solicitar presupuesto
      </button>

      <button class="quick" data-message="Quiero hablar con el equipo.">
        Hablar con el equipo
      </button>

      <div class="side-footer">
        <span class="dot"></span>
        Demo preparada para presentación
      </div>

    </aside>


    <!-- CONTENIDO PRINCIPAL -->
    <main class="main">

      <header class="topbar">

        <button class="mobile-menu" id="mobileMenu">
          ☰
        </button>

        <div>
          <strong>Oxymar IA</strong>
          <span>● En línea · Demo</span>
        </div>

        <button class="more" id="more">
          •••
        </button>

      </header>


      <!-- CHAT -->
      <section class="chat" id="chat">

        <div class="welcome" id="welcome">

          <div class="welcome-icon">
            ✦
          </div>

          <h1>
            Hola, soy el asistente de Oxymar.
          </h1>

          <p>
            Puedo ayudarte con información, servicios,
            presupuestos y contacto con el equipo.
          </p>

        </div>


        <div class="suggestions" id="suggestions">

          <button data-message="¿Qué servicios ofrece Oxymar?">
            ¿Qué servicios ofrece Oxymar?
          </button>

          <button data-message="Quiero solicitar un presupuesto">
            Quiero un presupuesto
          </button>

          <button data-message="Quiero hablar con una persona">
            Hablar con una persona
          </button>

        </div>

      </section>


      <!-- ESCRIBIR -->
      <div class="composer-wrap">

        <div class="composer">

          <input
            id="input"
            type="text"
            placeholder="Escribe tu mensaje..."
            autocomplete="off"
          >

          <button id="send" aria-label="Enviar">
            ➤
          </button>

        </div>

        <small>
          Demo · Las respuestas actuales son simuladas para la presentación.
        </small>

      </div>

    </main>

  </div>

  <script src="app.js"></script>

</body>
</html>
:root {
  --navy: #0b1b2b;
  --navy-2: #12283b;
  --teal: #16b6a5;
  --teal-dark: #0b9f90;

  --background: #f5f7fa;
  --text: #152333;
  --muted: #718096;

  --white: #ffffff;
  --line: #e5eaf0;
}


* {
  box-sizing: border-box;
}


html,
body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}


body {
  font-family:
    Inter,
    ui-sans-serif,
    system-ui,
    -apple-system,
    BlinkMacSystemFont,
    "Segoe UI",
    sans-serif;

  color: var(--text);
  background: var(--background);
}


button,
input {
  font: inherit;
}


button {
  cursor: pointer;
}


/* APP */

.app {
  display: flex;
  width: 100%;
  height: 100vh;
  min-height: 620px;
}


/* SIDEBAR */

.sidebar {
  width: 270px;

  background: var(--navy);
  color: white;

  padding: 24px 18px;

  display: flex;
  flex-direction: column;

  gap: 10px;
}


.brand {
  display: flex;
  align-items: center;

  gap: 12px;

  margin: 4px 8px 28px;
}


.brand-mark {
  width: 40px;
  height: 40px;

  border-radius: 12px;

  background: var(--teal);

  display: grid;
  place-items: center;

  font-weight: 800;
  font-size: 20px;
}


.brand strong {
  display: block;
}


.brand span {
  display: block;

  margin-top: 2px;

  font-size: 12px;

  color: #9fb0c2;
}


.new-chat {
  border: 1px solid #294052;

  background: var(--navy-2);

  color: white;

  border-radius: 12px;

  padding: 13px;

  text-align: left;

  transition: 0.2s;
}


.new-chat:hover {
  background: #19364c;
}


.side-label {
  font-size: 11px;

  text-transform: uppercase;

  letter-spacing: 0.12em;

  color: #70879b;

  margin: 24px 10px 5px;
}


.quick {
  background: transparent;

  border: 0;

  color: #cbd7e1;

  text-align: left;

  padding: 11px 10px;

  border-radius: 9px;

  transition: 0.2s;
}


.quick:hover {
  background: var(--navy-2);

  color: white;
}


.side-footer {
  margin-top: auto;

  color: #7890a4;

  font-size: 11px;

  padding: 10px;
}


.dot {
  display: inline-block;

  width: 7px;
  height: 7px;

  background: #2bd3a8;

  border-radius: 50%;

  margin-right: 6px;
}


/* MAIN */

.main {
  flex: 1;

  display: flex;
  flex-direction: column;

  min-width: 0;
}


/* TOPBAR */

.topbar {
  height: 72px;

  background: white;

  border-bottom: 1px solid var(--line);

  display: flex;

  align-items: center;

  justify-content: space-between;

  padding: 0 28px;
}


.topbar strong {
  display: block;
}


.topbar span {
  display: block;

  font-size: 12px;

  color: #32a58e;

  margin-top: 3px;
}


.more,
.mobile-menu {
  border: 0;

  background: transparent;

  color: #607286;

  font-size: 20px;
}


.mobile-menu {
  display: none;
}


/* CHAT */

.chat {
  flex: 1;

  overflow-y: auto;

  padding: 55px 24px 170px;

  max-width: 900px;

  width: 100%;

  margin: auto;
}


/* WELCOME */

.welcome {
  text-align: center;

  max-width: 650px;

  margin: 20px auto 34px;
}


.welcome-icon {
  width: 56px;
  height: 56px;

  border-radius: 18px;

  background: #dff7f3;

  color: var(--teal-dark);

  display: grid;
  place-items: center;

  margin: 0 auto 20px;

  font-size: 25px;
}


.welcome h1 {
  font-size: 32px;

  line-height: 1.15;

  margin: 0 0 12px;
}


.welcome p {
  color: var(--muted);

  line-height: 1.6;

  margin: 0;
}


/* SUGERENCIAS */

.suggestions {
  display: flex;

  flex-wrap: wrap;

  justify-content: center;

  gap: 10px;
}


.suggestions button {
  background: white;

  border: 1px solid var(--line);

  border-radius: 20px;

  padding: 10px 15px;

  color: #405266;

  transition: 0.2s;
}


.suggestions button:hover {
  border-color: #9bded7;

  color: var(--teal-dark);
}


/* MENSAJES */

.message {
  display: flex;

  margin: 18px 0;
}


.message.user {
  justify-content: flex-end;
}


.bubble {
  max-width: min(72%, 650px);

  padding: 13px 16px;

  border-radius: 16px;

  line-height: 1.5;

  box-shadow: 0 1px 2px rgba(11, 27, 43, 0.05);
}


.assistant .bubble {
  background: white;

  border: 1px solid var(--line);

  border-top-left-radius: 5px;
}


.user .bubble {
  background: var(--navy);

  color: white;

  border-top-right-radius: 5px;
}


/* TYPING */

.typing {
  display: flex;

  gap: 4px;

  padding: 6px;
}


.typing i {
  width: 6px;
  height: 6px;

  background: #9aa8b6;

  border-radius: 50%;

  animation: typing 1s infinite;
}


.typing i:nth-child(2) {
  animation-delay: 0.15s;
}


.typing i:nth-child(3) {
  animation-delay: 0.3s;
}


@keyframes typing {
  50% {
    opacity: 0.3;

    transform: translateY(-2px);
  }
}


/* COMPOSER */

.composer-wrap {
  position: fixed;

  bottom: 0;

  left: 270px;

  right: 0;

  background:
    linear-gradient(
      transparent,
      var(--background) 30%
    );

  padding: 38px 24px 20px;
}


.composer {
  max-width: 900px;

  margin: auto;

  background: white;

  border: 1px solid #dfe6ed;

  border-radius: 16px;

  display: flex;

  padding: 6px 7px 6px 16px;

  box-shadow:
    0 10px 35px rgba(11, 27, 43, 0.07);
}


.composer input {
  flex: 1;

  border: 0;

  outline: 0;

  background: transparent;

  min-width: 0;
}


.composer button {
  width: 42px;
  height: 42px;

  border: 0;

  border-radius: 12px;

  background: var(--teal);

  color: white;

  transition: 0.2s;
}


.composer button:hover {
  background: var(--teal-dark);

  transform: translateY(-1px);
}


.composer-wrap small {
  display: block;

  text-align: center;

  color: #8a98a8;

  font-size: 10px;

  margin-top: 8px;
}


/* MÓVIL */

@media (max-width: 700px) {

  .sidebar {
    position: fixed;

    z-index: 5;

    left: -290px;

    top: 0;
    bottom: 0;

    transition: 0.2s;
  }


  .sidebar.open {
    left: 0;
  }


  .mobile-menu {
    display: block;
  }


  .topbar {
    padding: 0 16px;
  }


  .chat {
    padding: 35px 16px 170px;
  }


  .welcome h1 {
    font-size: 27px;
  }


  .bubble {
    max-width: 86%;
  }


  .composer-wrap {
    left: 0;

    padding: 28px 12px 14px;
  }

}
const chat = document.getElementById("chat");
const input = document.getElementById("input");
const send = document.getElementById("send");


// RESPUESTAS DE LA DEMO

const responses = [

  {
    keys: ["servicio", "servicios"],
    text:
      "Claro. En esta demo puedo presentar los principales servicios de Oxymar y orientar al cliente según lo que necesite. En la versión real, esta respuesta se conectará a la información y documentación de la empresa."
  },

  {
    keys: [
      "presupuesto",
      "precio",
      "cotización",
      "cotizacion"
    ],
    text:
      "Perfecto. Puedo recoger los datos necesarios para preparar una solicitud de presupuesto y derivarla al equipo de Oxymar. Para la demo, podemos simular ese proceso completo."
  },

  {
    keys: [
      "persona",
      "equipo",
      "humano",
      "hablar"
    ],
    text:
      "Por supuesto. Puedo derivarte al equipo de Oxymar. En una versión real, aquí podríamos conectar WhatsApp, correo, CRM o incluso una llamada telefónica."
  },

  {
    keys: [
      "hola",
      "buenas",
      "hey"
    ],
    text:
      "¡Hola! 👋 Soy el asistente de Oxymar. ¿En qué puedo ayudarte hoy?"
  }

];


// AÑADIR MENSAJE

function addMessage(text, type) {

  const row = document.createElement("div");

  row.className = "message " + type;


  const bubble = document.createElement("div");

  bubble.className = "bubble";

  bubble.textContent = text;


  row.appendChild(bubble);

  chat.appendChild(row);


  chat.scrollTop = chat.scrollHeight;
}


// BUSCAR RESPUESTA

function getReply(question) {

  const low = question.toLowerCase();


  const found = responses.find(response =>
    response.keys.some(key =>
      low.includes(key)
    )
  );


  if (found) {
    return found.text;
  }


  return (
    "Entendido. Puedo ayudarte con información sobre Oxymar, " +
    "solicitudes de presupuesto o contacto con el equipo. " +
    "Para la presentación, esta demo simula el flujo; " +
    "después podemos conectar una IA real y los canales de la empresa."
  );
}


// ENVIAR PREGUNTA

function ask(question) {

  question = question.trim();


  if (!question) {
    return;
  }


  // Quitamos pantalla inicial

  const welcome = document.getElementById("welcome");

  const suggestions =
    document.getElementById("suggestions");


  if (welcome) {
    welcome.remove();
  }


  if (suggestions) {
    suggestions.remove();
  }


  // Mensaje usuario

  addMessage(question, "user");


  input.value = "";


  // Indicador escribiendo

  const row =
    document.createElement("div");


  row.className =
    "message assistant";


  row.innerHTML =
    `
      <div class="bubble">
        <div class="typing">
          <i></i>
          <i></i>
          <i></i>
        </div>
      </div>
    `;


  chat.appendChild(row);

  chat.scrollTop =
    chat.scrollHeight;


  // Respuesta simulada

  setTimeout(() => {

    row.querySelector(".bubble").textContent =
      getReply(question);

    chat.scrollTop =
      chat.scrollHeight;

  }, 650);
}


// BOTÓN ENVIAR

send.addEventListener("click", () => {

  ask(input.value);

});


// ENTER

input.addEventListener("keydown", event => {

  if (event.key === "Enter") {

    ask(input.value);

  }

});


// BOTONES DE SUGERENCIAS

document
  .querySelectorAll("[data-message]")
  .forEach(button => {

    button.addEventListener("click", () => {

      ask(button.dataset.message);

    });

  });


// NUEVA CONVERSACIÓN

document
  .getElementById("newChat")
  .addEventListener("click", () => {

    location.reload();

  });


// MENÚ SUPERIOR

document
  .getElementById("more")
  .addEventListener("click", () => {

    alert(
      "Oxymar IA — Demo\n\n" +
      "Aquí podremos añadir configuración, " +
      "historial y conexión con los sistemas de la empresa."
    );

  });


// MENÚ MÓVIL

document
  .getElementById("mobileMenu")
  .addEventListener("click", () => {

    document
      .getElementById("sidebar")
      .classList.toggle("open");

  });
{
  "name": "oxi-demo",
  "version": "1.0.0",
  "description": "Demo del asistente de IA de Oxymar",
  "private": true,
  "scripts": {
    "start": "npx serve ."
  }
}
# Oxymar IA — Demo

Demo visual del asistente de inteligencia artificial de Oxymar.

## Archivos

- `index.html` — estructura de la aplicación.
- `styles.css` — diseño y versión responsive.
- `app.js` — funcionamiento del chat y respuestas simuladas.
- `package.json` — configuración básica para ejecutar la demo.
- `README.md` — documentación.

## Cómo probarla

La forma más sencilla es abrir:

`index.html`

directamente en un navegador.

También se puede ejecutar con Node.js:

```bash
npm install
npm start