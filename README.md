# 🚀 Workshop: Build Intelligent Apps Faster

## Desarrollo de Aplicaciones Modernas con GitHub Copilot, Azure OpenAI y Azure Container Apps

![GitHub Copilot](https://img.shields.io/badge/GitHub%20Copilot-Enabled-green)
![Python](https://img.shields.io/badge/Python-3.12+-blue)
![React](https://img.shields.io/badge/React-19+-61DAFB)
![Azure](https://img.shields.io/badge/Azure-Container%20Apps-0078D4)
![Azure OpenAI](https://img.shields.io/badge/Azure%20OpenAI-GPT--4o-orange)

---

**Duración:** 3 horas
**Audiencia:** Arquitectos, Developers senior, DevOps, Líderes técnicos
**Nivel:** Intermedio

---

## 📋 Tabla de Contenidos

- [Introducción](#-introducción)
- [Conceptos Clave de GitHub Copilot](#-conceptos-clave-de-github-copilot)
- [Pre-requisitos](#-pre-requisitos)
- [Agenda del Workshop](#-agenda-del-workshop)
- [Módulo 1: Backend API con Python y GitHub Copilot](#-módulo-1--backend-api-con-python-y-github-copilot-40-min)
- [Módulo 2: Agente Inteligente con Azure OpenAI](#-módulo-2--agente-inteligente-con-azure-openai-25-min)
- [Módulo 3: Frontend con React y GitHub Copilot](#-módulo-3--frontend-con-react-y-github-copilot-30-min)
- [Módulo 4: Containerización con Docker](#-módulo-4--containerización-con-docker-15-min)
- [Módulo 5: Infraestructura con Azure Bicep](#-módulo-5--infraestructura-con-azure-bicep-25-min)
- [Módulo 6: CI/CD con GitHub Actions](#-módulo-6--cicd-con-github-actions-20-min)
- [Checklist Final](#-checklist-final)
- [Recursos Adicionales](#-recursos-adicionales)

---

## 🎯 Introducción

Este workshop práctico te guiará en la construcción de una **aplicación inteligente para Contoso Financial Services** — un agente de IA que responde preguntas de clientes sobre servicios financieros en lenguaje natural.

Construirás desde cero:

- ✅ Una **REST API en Python** (FastAPI) con GitHub Copilot
- ✅ Un **agente inteligente** usando Azure OpenAI (GPT-4o)
- ✅ Un **frontend en React** con interfaz de chat
- ✅ **Containerización** con Docker
- ✅ **Infraestructura como Código** con Azure Bicep
- ✅ **CI/CD automatizado** con GitHub Actions
- ✅ **Despliegue en Azure** Container Registry + Container Apps

### Estándares del Proyecto

| Aspecto | Estándar |
|---------|----------|
| Backend | Python 3.12+ / FastAPI |
| Frontend | Node.js 20+ / React 19 / Vite |
| AI | Azure OpenAI (GPT-4o) |
| Contenedores | Docker / Azure Container Registry |
| Plataforma | Azure Container Apps |
| IaC | Azure Bicep |
| CI/CD | GitHub Actions |
| Idioma | Documentación y UI en español, código en inglés |

### Escenario: Contoso Financial Services

Contoso es una empresa de servicios financieros que necesita un asistente virtual inteligente para atender consultas de clientes sobre:

- 💳 Productos financieros (cuentas, tarjetas, préstamos, inversiones)
- 📊 Tasas de interés y comisiones
- 🔒 Procesos de seguridad y prevención de fraude
- 📋 Requisitos y trámites
- 💡 Asesoría financiera general

---

## 🧠 Conceptos Clave de GitHub Copilot

### Modos de GitHub Copilot Chat

GitHub Copilot tiene tres modos principales de operación:

#### 1️⃣ Modo Ask (Preguntar) 💬

| | |
|---|---|
| **Ícono** | 💬 Burbuja de mensaje |
| **Función** | Solo responde preguntas, NO modifica archivos |
| **Uso ideal** | Explorar, entender, planificar, aprender |

#### 2️⃣ Modo Agent (Agente) 🤖

| | |
|---|---|
| **Ícono** | 🤖 Robot o chispa |
| **Función** | PUEDE crear y modificar archivos automáticamente |
| **Uso ideal** | Implementar cambios, crear código, refactorizar |

#### 3️⃣ Modo Plan (Planificar) 📋

| | |
|---|---|
| **Ícono** | 📋 Lista o documento |
| **Función** | Genera un plan detallado ANTES de ejecutar |
| **Uso ideal** | Tareas complejas que involucran múltiples archivos |

#### Comparativa de Modos

| Característica | Ask 💬 | Agent 🤖 | Plan 📋 |
|---|---|---|---|
| Modifica archivos | ❌ No | ✅ Sí | ✅ Sí (con aprobación) |
| Velocidad | Rápido | Rápido | Más lento |
| Control | N/A | Bajo | Alto |
| Ideal para | Aprender | Implementar | Tareas complejas |

### ¿Qué es @workspace?

El `@workspace` proporciona contexto sobre todo tu espacio de trabajo a GitHub Copilot.

| Uso | Ejemplo |
|---|---|
| Buscar código | `@workspace ¿dónde se define el endpoint de chat?` |
| Entender el proyecto | `@workspace ¿qué hace este proyecto?` |
| Generar código contextual | `@workspace crea un nuevo endpoint similar a los existentes` |

### Agentes Personalizados (@nombre-agente)

Los agentes personalizados son "expertos" que puedes crear para tareas específicas. Se definen en archivos Markdown en `.github/agents/`.

**¿Cómo funcionan?**
1. Creas un archivo `.github/agents/mi-agente.md`
2. Defines el rol, reglas y conocimiento del agente
3. Lo invocas con `@mi-agente` en el chat

### Comandos Especiales (/comando)

| Comando | Función | Ejemplo |
|---|---|---|
| `/tests` | Genera pruebas unitarias | Selecciona código → `/tests` |
| `/doc` | Genera documentación | Selecciona función → `/doc` |
| `/fix` | Propone corrección de errores | Selecciona código con error → `/fix` |
| `/explain` | Explica código seleccionado | Selecciona código → `/explain` |

---

## 🛠️ Pre-requisitos

### Software Necesario

```bash
# Verificar instalaciones
python3 --version   # 3.12 o superior
node --version      # 20.x o superior
npm --version       # 10.x o superior
docker --version    # Docker Desktop
az --version        # Azure CLI 2.60+
git --version       # Git
code --version      # Visual Studio Code
```

### Extensiones de VS Code

1. **GitHub Copilot** — Extensión principal
2. **GitHub Copilot Chat** — Chat integrado
3. **Python** — Soporte para Python
4. **Pylance** — IntelliSense avanzado para Python
5. **ES7+ React/Redux/React-Native** — Snippets para React
6. **Docker** — Soporte para contenedores
7. **Bicep** — Soporte para Azure Bicep
8. **Azure Tools** — Herramientas de Azure

### Cuentas Necesarias

- ✅ **GitHub** con acceso a GitHub Copilot (individual, organización o educativa)
- ✅ **Azure** con suscripción activa y acceso a Azure OpenAI
- ✅ **Docker Hub** (opcional, usaremos Azure Container Registry)

---

## 📅 Agenda del Workshop

| Tiempo | Módulo | Contenido | Modo Copilot |
|---|---|---|---|
| 0:00 - 0:10 | Introducción | Setup y configuración | — |
| 0:10 - 0:50 | Módulo 1 | Backend API en Python con FastAPI | Agent + Plan |
| 0:50 - 1:15 | Módulo 2 | Agente inteligente con Azure OpenAI | Ask + Agent |
| 1:15 - 1:25 | ☕ Break | Descanso | — |
| 1:25 - 1:55 | Módulo 3 | Frontend con React | @contoso-frontend |
| 1:55 - 2:10 | Módulo 4 | Containerización con Docker | Agent |
| 2:10 - 2:35 | Módulo 5 | Infraestructura con Azure Bicep | Agent + Plan |
| 2:35 - 2:55 | Módulo 6 | CI/CD con GitHub Actions | Agent |
| 2:55 - 3:00 | Cierre | Demo final y Q&A | — |

---

## 🔬 Módulo 1 — Backend API con Python y GitHub Copilot (40 min)

### Objetivos

- ✅ Configurar instrucciones de Copilot para el proyecto
- ✅ Crear una REST API con FastAPI usando GitHub Copilot
- ✅ Implementar endpoints de salud, productos financieros y chat
- ✅ Usar Modo Agent y Modo Plan efectivamente

### Paso 1.1: Crear instrucciones de Copilot

> ⚠️ **IMPORTANTE:** Este paso debe ejecutarse ANTES de crear código para que Copilot siga los estándares desde el inicio.

🤖 **PROMPT en Modo Agent:**

```
Crea el archivo .github/copilot-instructions.md con instrucciones para que Copilot actúe como experto en desarrollo full-stack para Contoso Financial Services:

# Instrucciones para GitHub Copilot - Contoso Financial Services

## Idioma
- La documentación, comentarios, docstrings, mensajes de UI y respuestas de API deben estar en **español**
- El código (variables, funciones, clases, constantes) debe estar en **inglés**
- Nombres de archivos y carpetas en inglés

## Backend (Python)
| Aspecto | Estándar |
|---------|----------|
| Framework | FastAPI |
| Python | 3.12+ |
| Async | Usar async/await en todos los endpoints |
| Validación | Pydantic v2 para modelos y esquemas |
| Estructura | Modular por dominio (routers, models, services) |

## Frontend (React)
| Aspecto | Estándar |
|---------|----------|
| Framework | React 19 con Vite |
| Lenguaje | TypeScript |
| Estilos | CSS Modules o Tailwind CSS |
| Estado | React hooks (useState, useEffect, useContext) |

## Nomenclatura Python
- Funciones y variables: snake_case en inglés (get_products, create_query)
- Clases: PascalCase en inglés (FinancialProduct, CustomerQuery)
- Constantes: UPPER_SNAKE_CASE (BASE_RATE, MAX_RETRIES)

## Nomenclatura React
- Componentes: PascalCase (ChatPanel, ProductCard)
- Hooks: camelCase con prefijo use (useChat, useProducts)
- Archivos: PascalCase.tsx para componentes

## Seguridad
- Nunca exponer claves API en código fuente
- Usar variables de entorno para configuración sensible
- Validar todas las entradas del usuario
- Sanitizar respuestas del modelo AI antes de mostrar

## Documentación
- Docstrings en español para todas las funciones públicas
- Type hints en todas las funciones Python
- JSDoc/TSDoc para componentes React principales
```

### Paso 1.2: Crear estructura del proyecto

🤖 **PROMPT en Modo Agent:**

```
Crea la estructura de un proyecto monorepo con backend
Python/FastAPI en src/backend y frontend React en src/frontend.
Incluye también carpetas para test, docs, infra (Bicep) y .github.
Genera el requirements.txt con las dependencias necesarias para
FastAPI y Azure OpenAI, y un .env.example con las variables
de Azure OpenAI.
```

### Paso 1.3: Implementar configuración y modelos

🤖 **PROMPT en Modo Agent:**

```
Implementa la configuración del backend usando pydantic-settings
para cargar las variables de Azure OpenAI desde el .env.
Crea también los modelos Pydantic necesarios para:
productos financieros, mensajes de chat (request/response)
y health check.
```

### Paso 1.4: Implementar endpoint de salud

🤖 **PROMPT en Modo Agent:**

```
Crea un endpoint de health check en /api/health que retorne
el estado del servicio de Contoso Financial Services.
Incluye un endpoint /api/health/ready que verifique que
las variables de entorno estén configuradas.
```

### Paso 1.5: Implementar endpoint de productos financieros

🤖 **PROMPT en Modo Agent:**

```
Crea un endpoint en /api/products con datos de ejemplo
hardcodeados de al menos 6 productos de Contoso
(cuentas de ahorro, tarjetas de crédito, préstamos
e inversiones con sus tasas y comisiones).
Incluye un GET para listar todos con filtro por tipo
y un GET por ID.

Productos de ejemplo:
- Cuenta Contoso Plus (cuenta de ahorro, 4.5% anual)
- Cuenta Contoso Empresarial (cuenta corriente empresarial)
- Tarjeta Contoso Gold (tarjeta de crédito, tasa 28.9%)
- Tarjeta Contoso Platinum (tarjeta premium, beneficios viajero)
- Préstamo Contoso Personal (préstamo personal, tasa 12.5%)
- Inversión Contoso Crecimiento (fondo de inversión, rendimiento 8.2%)
```

### Paso 1.6: Implementar el archivo principal

🤖 **PROMPT en Modo Agent:**

```
Crea el archivo principal de la aplicación FastAPI para
Contoso Financial Services. Configura CORS para desarrollo
local (puertos 5173 y 3000) y registra los routers de health
y products que acabamos de crear.
```

### Paso 1.7: Ejecutar y probar la API

🤖 **PROMPT en Modo Agent:**

```
Ejecuta la API de backend:
cd src/backend
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

📝 **Alternativa manual:**

```bash
cd src/backend
python -m venv venv
source venv/bin/activate  # macOS/Linux
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000
```

Abre en el navegador: `http://localhost:8000/docs`

✅ **Verificar:**
- Swagger UI muestra todos los endpoints
- GET `/api/health` retorna estado saludable
- GET `/api/products` retorna los 6 productos de Contoso

### 🛠️ Troubleshooting Módulo 1

| Problema | Solución |
|---|---|
| `ModuleNotFoundError` | Verifica que el virtualenv está activado y ejecuta `pip install -r requirements.txt` |
| Puerto 8000 en uso | Cambia el puerto: `uvicorn app.main:app --reload --port 8001` |
| Error de importación | Verifica que existan `__init__.py` en todas las carpetas |
| Swagger no carga | Asegúrate de acceder a `http://localhost:8000/docs` |

---

## 🔬 Módulo 2 — Agente Inteligente con Azure OpenAI (25 min)

### Objetivos

- ✅ Configurar la conexión con Azure OpenAI
- ✅ Crear el servicio del agente de Contoso Financial Services
- ✅ Implementar el endpoint de chat con contexto financiero
- ✅ Probar el agente con consultas en lenguaje natural

### Paso 2.1: Crear recursos de Azure OpenAI con Azure CLI

> 💡 **NOTA:** Vamos a usar GitHub Copilot para que nos genere los comandos de Azure CLI y los ejecutamos directamente en la terminal. No necesitas crear archivos adicionales.

📍 **1. Inicia sesión en Azure:**

```bash
az login
```

🤖 **PROMPT en Modo Agent:**

```
Usando Azure CLI ejecuta en la terminal los siguientes pasos:

1. Crea un Grupo de Recursos llamado "rg-contoso-taller" en la región EastUS2
2. Provisiona un servicio de Azure OpenAI en ese grupo de recursos
3. Despliega un modelo gpt-4o en el servicio
4. Obtén el endpoint y la clave API del servicio
5. Actualiza el archivo src/backend/.env con los valores obtenidos
```

> 📖 **Copilot ejecutará cada comando directamente en la terminal y actualizará tu `.env` automáticamente.**

📍 **2. Configura tu archivo `.env`:**

```bash
cp src/backend/.env.example src/backend/.env
```

Edita `src/backend/.env` con los valores reales que obtuviste de los comandos anteriores:

```env
AZURE_OPENAI_ENDPOINT=<tu-endpoint>
AZURE_OPENAI_API_KEY=<tu-clave-api>
AZURE_OPENAI_DEPLOYMENT=gpt-4o
AZURE_OPENAI_API_VERSION=2024-12-01-preview
```

✅ **Verificar:**
- El grupo de recursos aparece en Azure Portal
- El recurso de Azure OpenAI está creado y activo
- El modelo gpt-4o está desplegado
- El archivo `.env` tiene los valores correctos

### Paso 2.2: Diseñar e implementar el servicio de Azure OpenAI

> 💡 **CONCEPTO:** Primero vamos a entender qué necesitamos construir y luego le pedimos a Copilot que lo implemente.

🤖 **PROMPT en Modo Ask:**

```
¿Cómo debería diseñar un servicio en Python para conectarme a Azure OpenAI usando
el SDK oficial? Necesito:
- Una clase que se inicialice con las variables de entorno (endpoint, api_key, api_version)
- Un system prompt para un agente financiero llamado ContosoBot
- Un método async para chat que reciba mensaje e historial
- La API REST debe tener documentación Swagger automática con FastAPI

Explícame la arquitectura y qué patrones debo seguir.
```

> 📖 **Revisa la respuesta de Copilot** — entiende la arquitectura propuesta antes de implementar.

🤖 **PROMPT en Modo Agent:**

```
Implementa lo que acabamos de discutir. Crea el archivo src/backend/app/services/openai_service.py con:

1. Clase OpenAIService que:
   - Se inicialice con AzureOpenAI client usando las variables de entorno (endpoint, api_key, api_version)
   - Tenga un system prompt detallado para el agente de Contoso Financial Services:
     
     "Eres el asistente virtual de Contoso Financial Services. Tu nombre es ContosoBot.
     Eres experto en servicios financieros y ayudas a los clientes con:
     - Información sobre productos (cuentas, tarjetas, préstamos, inversiones)
     - Consultas sobre tasas de interés y comisiones
     - Requisitos para apertura de cuentas y solicitud de créditos
     - Asesoría financiera general
     - Procesos de seguridad y prevención de fraude
     
     Reglas:
     - Responde SIEMPRE en español
     - Sé amable, profesional y conciso
     - Si no sabes algo, indícalo honestamente
     - Nunca inventes tasas o condiciones específicas
     - Sugiere al cliente contactar a un asesor para operaciones complejas
     - No proporciones asesoría fiscal o legal específica
     
     Productos de Contoso disponibles:
     - Cuenta Contoso Plus: cuenta de ahorro, 4.5% anual, sin comisión con saldo mínimo de $5,000
     - Cuenta Contoso Empresarial: cuenta corriente, sin rendimiento, comisión $350/mes
     - Tarjeta Contoso Gold: crédito, CAT 42.5%, anualidad $1,200
     - Tarjeta Contoso Platinum: crédito premium, CAT 38.2%, anualidad $3,500, seguro viajero incluido
     - Préstamo Contoso Personal: tasa desde 12.5% anual, plazo 12-60 meses
     - Inversión Contoso Crecimiento: fondo diversificado, rendimiento histórico 8.2% anual"

   - Método async chat(message: str, history: list) que:
     - Construya la lista de mensajes con el system prompt + history + message nuevo
     - Llame a client.chat.completions.create() con el modelo configurado
     - Retorne la respuesta y tokens usados
     - Maneje errores con try/except y mensajes descriptivos

2. Instancia global del servicio (singleton)

Asegúrate de que todos los modelos de datos tengan ejemplos para la documentación
automática de Swagger (schema_extra / model_config).
```

### Paso 2.3: Diseñar e implementar el endpoint de chat

🤖 **PROMPT en Modo Ask:**

```
¿Cuál es la mejor forma de estructurar un endpoint de chat con FastAPI que use
el servicio de Azure OpenAI que ya creamos? Necesito:
- Un endpoint POST que reciba mensaje e historial
- Un endpoint para limpiar historial
- Que la documentación Swagger se genere automáticamente con ejemplos
- Buenas prácticas de manejo de errores HTTP

Explícame cómo estructurar el router y qué modelos de datos necesito.
```

> 📖 **Revisa la respuesta de Copilot** — confirma que la estructura propuesta tiene sentido.

🤖 **PROMPT en Modo Agent:**

```
Implementa lo que discutimos. Crea el archivo src/backend/app/routers/chat.py con:

1. Router de FastAPI con prefix "/api/chat" y tag "Chat IA"

2. POST /api/chat - Endpoint principal del agente
   - Recibe: ChatRequest (message + history opcional)
   - Usa OpenAIService para generar respuesta
   - Retorna: ChatResponse (response + tokens_used)
   - Manejo de errores con HTTPException

3. DELETE /api/chat/history - Limpia el historial (retorna confirmación)

4. Documentación completa para Swagger con:
   - Descripción de cada endpoint
   - Ejemplos de solicitud y respuesta en los modelos (schema_extra / model_config)
   - Códigos de error posibles (400, 500)
   - Tags y summary descriptivos
```

### Paso 2.4: Registrar el router de chat en main.py

🤖 **PROMPT en Modo Agent:**

```
@workspace Actualiza src/backend/app/main.py para incluir el router de chat.
Asegúrate de que el router de chat esté registrado junto con health y products.
```

### Paso 2.5: Probar el agente desde la terminal

Reinicia la API y verifica que Swagger funcione en `http://localhost:8000/docs`.

🤖 **PROMPT en Modo Ask:**

```
Genérame 5 comandos curl para probar el endpoint POST /api/chat de mi API
que corre en http://localhost:8000. Cada uno debe ser una pregunta diferente
que un cliente haría al agente de Contoso Financial Services:
1. Preguntar por cuentas de ahorro
2. Información sobre la Tarjeta Contoso Platinum
3. Requisitos para un préstamo personal
4. Comparar productos de inversión
5. Una pregunta con historial de conversación previo

Dame los comandos listos para copiar y pegar en la terminal.
```

> 📖 **Copia los comandos que Copilot te genere y ejecútalos directamente en la terminal.**

📍 **Ejemplo de ejecución en terminal:**

```bash
# Prueba 1: Consultar cuentas de ahorro
curl -s -X POST http://localhost:8000/api/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "¿Qué cuentas de ahorro tienen disponibles?", "history": []}' | python -m json.tool

# Prueba 2: Información de tarjeta
curl -s -X POST http://localhost:8000/api/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "Me interesa la Tarjeta Contoso Platinum, ¿qué beneficios tiene?", "history": []}' | python -m json.tool

# Prueba 3: Con historial de conversación
curl -s -X POST http://localhost:8000/api/chat \
  -H "Content-Type: application/json" \
  -d '{"message": "¿Y cuál es la anualidad?", "history": [{"role": "user", "content": "Háblame de la Tarjeta Gold"}, {"role": "assistant", "content": "La Tarjeta Contoso Gold es una tarjeta de crédito con CAT 42.5%."}]}' | python -m json.tool
```

✅ **Verificar:**
- El agente responde en español
- Las respuestas son coherentes con los productos de Contoso
- El historial de conversación funciona correctamente (prueba 3)
- Los tokens usados se reportan en la respuesta
- Swagger UI (`http://localhost:8000/docs`) muestra los endpoints documentados con ejemplos

### 🛠️ Troubleshooting Módulo 2

| Problema | Solución |
|---|---|
| Error 401 de Azure OpenAI | Verifica la API key en el archivo `.env` |
| Error "deployment not found" | Confirma que el nombre del deployment coincide con `AZURE_OPENAI_DEPLOYMENT` |
| Respuestas en inglés | Verifica que el system prompt incluya "Responde SIEMPRE en español" |
| Timeout | Verifica conectividad a Azure y que el recurso OpenAI esté activo |

---

## 🔬 Módulo 3 — Frontend con React y GitHub Copilot (30 min)

### Objetivos

- ✅ Crear un agente personalizado para el frontend de Contoso
- ✅ Crear una aplicación React con Vite usando GitHub Copilot
- ✅ Implementar una interfaz de chat profesional
- ✅ Conectar el frontend con la API backend

### Paso 3.1: Crear el Agente de Frontend Contoso 🤖

> 💡 **CONCEPTO:** Los agentes personalizados permiten crear "expertos" especializados que Copilot puede usar para tareas específicas.

🤖 **PROMPT en Modo Agent:**

```
Crea el archivo .github/agents/contoso-frontend.md con un agente para desarrollo frontend:

# Agente: Frontend Contoso (@contoso-frontend)

## Rol
Eres un experto en desarrollo frontend para Contoso Financial Services.
Creas interfaces profesionales, modernas y accesibles para aplicaciones financieras.

## Idioma
- Documentación, comentarios y textos de interfaz en **español**
- Código (variables, funciones, clases) en **inglés**
- Usar terminología financiera en español para los textos de UI

## Tecnologías
- React 19 con Vite
- TypeScript
- CSS3 con variables personalizadas
- HTML5 semántico

## Paleta de Colores Corporativa Contoso
| Color | Hex | Uso |
|-------|-----|-----|
| Azul corporativo | #0078D4 | Headers, botones principales, enlaces |
| Azul oscuro | #002050 | Navbar, footer, texto principal |
| Verde éxito | #107C10 | Confirmaciones, indicadores positivos |
| Naranja acento | #FF8C00 | CTAs, alertas, badges |
| Gris fondo | #F5F5F5 | Fondos de secciones |
| Blanco | #FFFFFF | Cards, fondos principales |
| Gris texto | #323130 | Texto principal |
| Gris secundario | #605E5C | Texto secundario |

## Tipografía
- Headings: 'Segoe UI Semibold', system-ui
- Cuerpo: 'Segoe UI', system-ui, sans-serif
- Código: 'Cascadia Code', monospace

## Diseño de Chat
- Mensajes del usuario: burbuja azul (#0078D4), texto blanco, alineados a la derecha
- Mensajes del asistente: burbuja gris claro (#F5F5F5), texto oscuro, alineados a la izquierda
- Input de mensaje: borde redondeado, ícono de enviar
- Indicador de "escribiendo..." animado mientras espera respuesta

## Accesibilidad (WCAG AA)
- Contraste mínimo 4.5:1
- Elementos interactivos accesibles por teclado
- Atributos ARIA donde corresponda

## Reglas Importantes
1. SIEMPRE incluir estados de carga (spinners, skeletons)
2. SIEMPRE manejar errores con mensajes amigables para el usuario
3. Textos visibles para el usuario en español
4. SIEMPRE mostrar el nombre "ContosoBot" en las respuestas del agente
5. Diseño Mobile First y responsive
```

### Paso 3.2: Crear el proyecto React

🤖 **PROMPT en Modo Agent:**

```
Crea el proyecto frontend con React y Vite en la carpeta src/frontend:

1. Ejecuta en terminal:
   npm create vite@latest src/frontend -- --template react-ts
   cd src/frontend
   npm install

2. Instala dependencias adicionales:
   npm install axios

3. Limpia los archivos por defecto (elimina contenido genérico de App.tsx, App.css)
```

📝 **Alternativa manual:**

```bash
npm create vite@latest src/frontend -- --template react-ts
cd src/frontend
npm install
npm install axios
```

### Paso 3.3: Crear estilos corporativos de Contoso

🤖 **PROMPT con Agente:**

```
@contoso-frontend Crea los estilos CSS corporativos de Contoso
en src/frontend/src/styles/contoso.css.
Usa la paleta de colores definida en el agente.
Incluye estilos para el layout general, el componente de chat
(burbujas de mensajes, input, indicador de escritura)
y diseño responsive.
```

### Paso 3.4: Crear componentes del chat

🤖 **PROMPT con Agente:**

```
@contoso-frontend Crea los componentes React del chat en
src/frontend/src/components/: un header corporativo,
burbujas de mensaje (diferenciando usuario vs ContosoBot),
input de texto con envío por Enter, indicador de escritura
animado, y un panel principal que integre todo con estado,
llamadas a la API y auto-scroll. Todo con TypeScript.
```

### Paso 3.5: Crear servicio HTTP para la API

🤖 **PROMPT con Agente:**

```
@contoso-frontend Crea el servicio HTTP en
src/frontend/src/services/api.ts con axios para conectar
con el backend en http://localhost:8000.
Incluye las interfaces TypeScript para los tipos de datos
(chat, productos, health) y las funciones para enviar mensajes,
obtener productos y verificar salud de la API.
```

### Paso 3.6: Integrar todo en App.tsx

🤖 **PROMPT con Agente:**

```
@contoso-frontend Actualiza src/frontend/src/App.tsx para:

1. Importar los estilos de Contoso y los componentes

2. Layout principal con:
   - Encabezado corporativo de Contoso
   - Panel de Chat como contenido principal (ocupa toda la altura disponible)
   - Footer simple: "© 2025 Contoso Financial Services — Todos los derechos reservados"

3. Limpio, profesional y responsivo
```

### Paso 3.7: Ejecutar el frontend

🤖 **PROMPT en Modo Agent:**

```
Ejecuta el frontend de React:
cd src/frontend
npm run dev
```

📝 **Alternativa manual:**

```bash
cd src/frontend
npm run dev
```

Abre el navegador en `http://localhost:5173`

✅ **Verificar:**
- El header de Contoso se muestra correctamente
- La interfaz de chat carga sin errores
- Se pueden enviar mensajes al agente
- Las respuestas del agente aparecen con el nombre "ContosoBot"
- El indicador de escritura se muestra mientras espera

### 🛠️ Troubleshooting Módulo 3

| Problema | Solución |
|---|---|
| CORS error al conectar con API | Verifica que la API tiene CORS habilitado para `http://localhost:5173` |
| El agente @contoso-frontend no responde | Recarga VS Code después de crear el archivo del agente |
| Estilos no se aplican | Verifica la importación del CSS en App.tsx |
| axios error | Confirma que la API backend está corriendo en puerto 8000 |

---

## 🔬 Módulo 4 — Containerización con Docker (15 min)

### Objetivos

- ✅ Crear Dockerfiles para backend y frontend
- ✅ Crear Docker Compose para desarrollo local
- ✅ Verificar que los contenedores funcionan correctamente

### Paso 4.1: Containerizar el backend

🤖 **PROMPT en Modo Agent:**

```
Containeriza mi aplicación backend en src/backend.
Usa una imagen slim de Python, asegúrate de instalar
las dependencias y expón el puerto 8000.
Incluye un .dockerignore adecuado.
```

### Paso 4.2: Containerizar el frontend

🤖 **PROMPT en Modo Agent:**

```
Containeriza mi aplicación frontend en src/frontend.
Usa multi-stage build: primero compila con Node.js
y luego sirve con nginx en puerto 80.
Incluye la configuración de nginx para SPA y un .dockerignore.
```

### Paso 4.3: Docker Compose

🤖 **PROMPT en Modo Agent:**

```
Crea un docker-compose.yml que levante el backend (puerto 8000)
y el frontend (puerto 3000) juntos.
El frontend depende del backend.
Usa las variables de entorno del archivo .env del backend.
```

### Paso 4.4: Construir y probar

🤖 **PROMPT en Modo Agent:**

```
Construye y ejecuta los contenedores con Docker Compose:
docker compose up --build
```

📝 **Alternativa manual:**

```bash
docker compose up --build -d
docker compose ps
docker compose logs -f
```

✅ **Verificar:**
- Backend accesible en `http://localhost:8000/docs`
- Frontend accesible en `http://localhost:3000`
- El chat funciona end-to-end desde el contenedor

```bash
# Detener contenedores
docker compose down
```

### 🛠️ Troubleshooting Módulo 4

| Problema | Solución |
|---|---|
| Docker build falla | Verifica que Docker Desktop está corriendo |
| Error de permisos | En Linux/Mac: verifica permisos del socket Docker |
| Frontend no conecta a backend | Verifica la URL del backend en la config de nginx o env vars |
| Imagen muy grande | Asegúrate de usar multi-stage build y `.dockerignore` |

---

## 🔬 Módulo 5 — Infraestructura con Azure Bicep (25 min)

### Objetivos

- ✅ Crear plantillas Bicep para Azure Container Registry
- ✅ Crear plantillas Bicep para Azure Container Apps
- ✅ Desplegar infraestructura con Azure CLI
- ✅ Subir imágenes Docker a Azure Container Registry

### Paso 5.1: Crear la plantilla Bicep principal

🤖 **PROMPT en Modo Plan:**

```
Crea la infraestructura como código con Azure Bicep. Necesito los siguientes archivos:

1. infra/main.bicep - Archivo principal que orquesta todos los módulos:
   - Parámetros: location, environmentName, imagenBackendTag, imagenFrontendTag
   - Llama a los módulos de ACR, Container Apps Environment y Container Apps

2. infra/modules/acr.bicep - Azure Container Registry:
   - SKU: Basic
   - Admin user habilitado (para simplificar el workshop)
   - Output: loginServer, nombre, password

3. infra/modules/log-analytics.bicep - Log Analytics Workspace:
   - SKU: PerGB2018
   - Retención: 30 días
   - Output: workspaceId, workspaceKey

4. infra/modules/container-app-env.bicep - Container Apps Environment:
   - Conectado a Log Analytics
   - Output: environmentId

5. infra/modules/container-app-backend.bicep - Container App para el backend:
   - Imagen desde ACR
   - Ingress externo en puerto 8000
   - Variables de entorno para Azure OpenAI (como secrets)
   - Recursos: 0.5 CPU, 1Gi memoria
   - Min replicas: 1, Max replicas: 3

6. infra/modules/container-app-frontend.bicep - Container App para el frontend:
   - Imagen desde ACR
   - Ingress externo en puerto 80
   - Variable de entorno: API_URL apuntando al backend
   - Recursos: 0.25 CPU, 0.5Gi memoria
   - Min replicas: 1, Max replicas: 2

7. infra/main.bicepparam - Archivo de parámetros

Muéstrame el plan antes de ejecutar.
```

### Paso 5.2: Crear archivo de parámetros

🤖 **PROMPT en Modo Agent:**

```
Crea el archivo infra/main.bicepparam usando los parámetros
definidos en main.bicep.
Usa location eastus2, environment name contoso-financial,
y tag latest para las imágenes.
```

### Paso 5.3: Desplegar infraestructura con Azure CLI

🤖 **PROMPT en Modo Agent:**

```
Usando Azure CLI ejecuta en la terminal los siguientes pasos:
1. Inicia sesión en Azure (az login)
2. Crea el grupo de recursos rg-contoso-financial en eastus2
3. Despliega la infraestructura usando el template
   infra/main.bicep con los parámetros de
   infra/main.bicepparam
```

### Paso 5.4: Subir imágenes a Azure Container Registry

🤖 **PROMPT en Modo Agent:**

```
Usando Azure CLI y Docker, ejecuta en la terminal:
1. Obtén el nombre del ACR del deployment que acabamos
   de crear en rg-contoso-financial
2. Haz login al ACR
3. Construye y sube las imágenes del backend (./src/backend)
   y frontend (./src/frontend) al ACR con tag v1
```

### Paso 5.5: Configurar secrets y actualizar Container Apps

🤖 **PROMPT en Modo Agent:**

```
Usando Azure CLI ejecuta en la terminal:
1. Obtén los nombres de las Container Apps de backend
   y frontend del grupo rg-contoso-financial
2. Configura los secrets de Azure OpenAI (endpoint y API key)
   en la Container App del backend
3. Actualiza ambas Container Apps para que usen
   las imágenes v1 que subimos al ACR
4. Al terminar, muéstrame las URLs públicas de ambas aplicaciones
```

✅ **Verificar:**
- El backend responde en la URL de Azure
- El frontend carga y se conecta al backend
- El chat con el agente funciona en producción

### 🛠️ Troubleshooting Módulo 5

| Problema | Solución |
|---|---|
| Error de Bicep "template validation failed" | Ejecuta `az bicep build --file infra/main.bicep` para ver errores |
| ACR login falla | Verifica que admin user está habilitado y ejecuta `az acr login` |
| Container App no inicia | Revisa logs: `az containerapp logs show --name APP --resource-group RG` |
| Error de image pull | Verifica las credenciales del ACR en Container App |
| Quota exceeded | Cambia a otra región o solicita incremento de cuota |

---

## 🔬 Módulo 6 — CI/CD con GitHub Actions (20 min)

### Objetivos

- ✅ Crear pipeline de CI para build y tests
- ✅ Crear pipeline de CD para deploy a Azure
- ✅ Configurar secretos en GitHub
- ✅ Implementar protección de environments

### Paso 6.1: Configurar secretos en GitHub

> 💡 **NOTA:** Antes de crear el pipeline, necesitas configurar los secretos en el repositorio de GitHub.

🤖 **PROMPT en Modo Agent:**

```
Usando Azure CLI, crea un Service Principal llamado
"sp-contoso-github-actions" con rol contributor sobre el
grupo de recursos rg-contoso-financial.
Muéstrame el JSON resultante y dime qué secretos necesito
configurar en GitHub Actions.
```

📍 **En GitHub → Settings → Secrets and variables → Actions**, agrega los secretos que Copilot te indique:

| Secreto | Valor |
|---|---|
| `AZURE_CREDENTIALS` | JSON del Service Principal |
| `ACR_LOGIN_SERVER` | URL del ACR (ej: contosofinancial.azurecr.io) |
| `ACR_USERNAME` | Username del ACR |
| `ACR_PASSWORD` | Password del ACR |
| `AZURE_OPENAI_ENDPOINT` | Endpoint de Azure OpenAI |
| `AZURE_OPENAI_API_KEY` | API Key de Azure OpenAI |
| `AZURE_OPENAI_DEPLOYMENT` | Nombre del deployment (ej: gpt-4o) |

### Paso 6.2: Crear pipeline CI/CD

🤖 **PROMPT en Modo Plan:**

```
Crea un pipeline CI/CD en .github/workflows/ci-cd.yml que:
testee backend (pytest) y frontend (build) en paralelo,
construya y suba las imágenes Docker al ACR en push a main,
y despliegue a las Container Apps con un environment protegido
"produccion" que requiera aprobación.
Usa los secretos que ya configuramos en GitHub.

Muéstrame el plan antes de ejecutar.
```

### Paso 6.3: Crear environment de producción en GitHub

📍 **En GitHub → Settings → Environments:**

1. Crear environment **"produccion"**
2. Agregar regla de protección: **Required reviewers** (agregar tu usuario)
3. Esto requiere aprobación manual antes de desplegar

### Paso 6.4: Probar el pipeline

```bash
# Hacer commit y push de todos los cambios
git add .
git commit -m "feat: workshop completo - Contoso Financial Services AI Agent"
git push origin main
```

Ve a **GitHub → Actions** para ver el pipeline ejecutándose.

✅ **Verificar:**
- Los jobs de test pasan correctamente
- Las imágenes se suben al ACR
- El deploy espera aprobación
- Después de aprobar, las Container Apps se actualizan

### Paso 6.5: Limpiar recursos (opcional)

> ⚠️ **IMPORTANTE:** Para evitar costos, destruye los recursos al terminar el workshop.

```bash
# Eliminar grupos de recursos
az group delete \
  --name rg-contoso-financial \
  --yes --no-wait

az group delete \
  --name rg-contoso-taller \
  --yes --no-wait

# Eliminar el Service Principal
az ad sp delete --id $(az ad sp list --display-name "sp-contoso-github-actions" --query "[0].id" -o tsv)
```

### 🛠️ Troubleshooting Módulo 6

| Problema | Solución |
|---|---|
| `AZURE_CREDENTIALS` inválido | Regenera el Service Principal y actualiza el secreto |
| Push al ACR falla | Verifica `ACR_LOGIN_SERVER`, `ACR_USERNAME` y `ACR_PASSWORD` |
| Deploy falla | Revisa logs: `az containerapp logs show --name APP --resource-group RG` |
| Tests fallan en CI | Verifica que las dependencias están en src/backend/requirements.txt / src/frontend/package.json |
| Environment no aparece | Los environments de protección requieren repo público o GitHub Pro/Team |

---

## ✅ Checklist Final

Al terminar el workshop, deberías tener:

### Configuración de Copilot
- [ ] `.github/copilot-instructions.md` — Instrucciones globales del proyecto
- [ ] `.github/agents/contoso-frontend.md` — Agente especializado en frontend

### Backend (Python/FastAPI)
- [ ] API REST funcional con FastAPI
- [ ] Endpoint de salud (`/api/health`)
- [ ] Endpoint de productos financieros (`/api/products`)
- [ ] Endpoint de chat con Azure OpenAI (`/api/chat`)
- [ ] Agente de Contoso Financial Services respondiendo en español
- [ ] Swagger/OpenAPI documentado

### Frontend (React)
- [ ] Aplicación React con Vite y TypeScript
- [ ] Interfaz de chat con estilo corporativo Contoso
- [ ] Burbujas de mensajes (usuario vs ContosoBot)
- [ ] Indicador de escritura animado
- [ ] Conexión funcional con el backend

### Containerización
- [ ] Dockerfile para backend (Python)
- [ ] Dockerfile para frontend (React + Nginx)
- [ ] Docker Compose para desarrollo local
- [ ] Ambos contenedores funcionan correctamente

### Infraestructura (Azure Bicep)
- [ ] Azure Container Registry creado
- [ ] Azure Container Apps Environment
- [ ] Container App para backend
- [ ] Container App para frontend
- [ ] Secrets configurados para Azure OpenAI

### CI/CD (GitHub Actions)
- [ ] Pipeline de tests (backend + frontend)
- [ ] Pipeline de build y push a ACR
- [ ] Pipeline de deploy a Azure Container Apps
- [ ] Environment de producción con protección

---

## 📖 Referencia Rápida

### Comandos Copilot

| Comando | Función | Ejemplo |
|---|---|---|
| `@workspace` | Contexto del proyecto | `@workspace ¿cómo se conecta el frontend al backend?` |
| `@contoso-frontend` | Agente de frontend | `@contoso-frontend crea un componente de tarjeta` |
| `/tests` | Generar pruebas | Selecciona código → `/tests` |
| `/doc` | Generar documentación | Selecciona función → `/doc` |
| `/fix` | Corregir errores | Selecciona error → `/fix` |
| `/explain` | Explicar código | Selecciona código → `/explain` |

### Atajos de Teclado

| Atajo | Función |
|---|---|
| `Ctrl+I` / `Cmd+I` | Abrir Copilot inline |
| `Ctrl+Shift+I` / `Cmd+Shift+I` | Abrir panel de Copilot Chat |
| `Tab` | Aceptar sugerencia |
| `Esc` | Rechazar sugerencia |
| `Alt+]` | Siguiente sugerencia |
| `Alt+[` | Sugerencia anterior |

### Comandos Azure CLI Útiles

```bash
# Login
az login

# Ver Container Apps
az containerapp list --resource-group rg-contoso-financial -o table

# Ver logs
az containerapp logs show --name NOMBRE_APP --resource-group rg-contoso-financial

# Ver revisiones
az containerapp revision list --name NOMBRE_APP --resource-group rg-contoso-financial -o table

# Scale manual
az containerapp update --name NOMBRE_APP --resource-group rg-contoso-financial --min-replicas 2 --max-replicas 5
```

---

## 📚 Recursos Adicionales

### Documentación Oficial

- [GitHub Copilot Docs](https://docs.github.com/en/copilot)
- [VS Code + Copilot](https://code.visualstudio.com/docs/copilot/overview)
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [React Documentation](https://react.dev/)
- [Azure OpenAI Service](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [Azure Container Apps](https://learn.microsoft.com/en-us/azure/container-apps/)
- [Azure Bicep](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/)
- [GitHub Actions](https://docs.github.com/en/actions)

### Azure OpenAI

- [Quickstart: Azure OpenAI con Python](https://learn.microsoft.com/en-us/azure/ai-services/openai/quickstart?pivots=programming-language-python)
- [Chat Completions API](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/chatgpt)
- [Modelos disponibles](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/models)

### Containerización

- [Dockerfile Best Practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
- [Azure Container Registry](https://learn.microsoft.com/en-us/azure/container-registry/)
- [Azure Container Apps](https://learn.microsoft.com/en-us/azure/container-apps/overview)

---

## 🙋 Preguntas Frecuentes

### ¿Por qué FastAPI y no Django o Flask?

FastAPI ofrece:
- **Async nativo** — Ideal para llamadas a Azure OpenAI
- **Validación automática** — Con Pydantic, las entradas se validan automáticamente
- **Swagger auto-generado** — Documentación de API sin esfuerzo adicional
- **Alto rendimiento** — Comparable a Node.js/Go

### ¿Puedo usar otro modelo de Azure OpenAI?

Sí. El workshop usa `gpt-4o` pero puedes usar:
- `gpt-4o-mini` — Más económico, rendimiento ligeramente menor
- `gpt-4.1` — Última generación, mejor seguimiento de instrucciones
- `gpt-4.1-mini` — Balance entre costo y rendimiento

Solo cambia la variable `AZURE_OPENAI_DEPLOYMENT` en tu `.env`.

### ¿Por qué Azure Bicep y no Terraform?

Para este workshop usamos Bicep porque:
- Es **nativo de Azure** — integración directa sin providers
- **Sintaxis más simple** que ARM templates
- **Sin estado remoto** — no requiere backend de estado
- GitHub Copilot tiene **excelente soporte** para Bicep

En producción, ambas opciones son válidas según las necesidades del equipo.

### ¿Cómo cambio la región de Azure?

Modifica el parámetro `location` en `infra/main.bicepparam`:

```bicep
param location = 'westus2'  // Cambia a la región deseada
```

Regiones recomendadas con Azure OpenAI: `eastus`, `eastus2`, `westus`, `swedencentral`.

### ¿Copilot no genera documentación en español o código en inglés?

1. Verifica que `.github/copilot-instructions.md` tenga la sección de **Idioma** correcta
2. Inclúyelo explícitamente en el prompt si es necesario
3. Usa `@workspace` para que tome contexto de los archivos existentes

### ¿Los agentes personalizados no funcionan?

- Verifica la ruta: `.github/agents/nombre-agente.md`
- El nombre del archivo (sin `.md`) es el nombre del agente
- **Recarga VS Code** después de crear el archivo
- Usa `@nombre-agente` al inicio del prompt

---

## 🏗️ Arquitectura de la Solución

```
┌──────────────────────────────────────────────────────┐
│                    GitHub Actions                     │
│          CI/CD Pipeline (test → build → deploy)       │
└──────────────────┬───────────────────────────────────┘
                   │
                   ▼
┌──────────────────────────────────────────────────────┐
│              Azure Container Registry                 │
│     contoso-backend:v1     contoso-frontend:v1        │
└──────────┬──────────────────────────┬────────────────┘
           │                          │
           ▼                          ▼
┌─────────────────────────────────────────────────────┐
│          Azure Container Apps Environment            │
│                                                      │
│  ┌─────────────────┐      ┌──────────────────┐      │
│  │   Backend App    │      │  Frontend App     │      │
│  │  (Python/FastAPI)│◄────▶│ (React/Nginx)     │      │
│  │   Port 8000     │      │   Port 80         │      │
│  └────────┬────────┘      └──────────────────┘      │
│           │                                          │
└───────────┼──────────────────────────────────────────┘
            │
            ▼
┌──────────────────────┐
│   Azure OpenAI       │
│   (GPT-4o)           │
│   Contoso Agent      │
└──────────────────────┘
```

---

## 👥 Créditos

**Workshop desarrollado por:** Armando Blanco

**Tecnologías:** GitHub Copilot, Python/FastAPI, React, Azure OpenAI, Azure Container Apps, Azure Bicep, GitHub Actions

**Duración:** 3 horas

**¿Preguntas o comentarios?** Contacta al equipo de capacitación.

---

## 📄 Licencia

Este workshop es material de capacitación. Uso educativo permitido.
