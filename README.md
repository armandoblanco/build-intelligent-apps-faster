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
Crea la estructura completa del proyecto monorepo:

1. Estructura general de carpetas:
   src/
   ├── backend/               ← API Python (FastAPI)
   │   ├── app/
   │   │   ├── main.py
   │   │   ├── config.py
   │   │   ├── routers/
   │   │   ├── models/
   │   │   └── services/
   │   ├── requirements.txt
   │   ├── .env.example
   │   └── Dockerfile
   └── frontend/              ← App React (Vite + TypeScript)
   test/                      ← Pruebas del proyecto
   docs/                      ← Documentación adicional
   infra/                     ← Infraestructura como código (Bicep)
   .github/                   ← Copilot instructions, agents, workflows
   docker-compose.yml

2. Archivo src/backend/requirements.txt con las dependencias:

3. Archivo src/backend/.env.example con las variables de entorno:
   - AZURE_OPENAI_ENDPOINT=https://tu-recurso.openai.azure.com/
   - AZURE_OPENAI_API_KEY=tu-clave-api
   - AZURE_OPENAI_DEPLOYMENT=gpt-4o
   - AZURE_OPENAI_API_VERSION=2024-12-01-preview
```

### Paso 1.3: Implementar configuración y modelos

🤖 **PROMPT en Modo Agent:**

```
Implementa los siguientes archivos del backend:

1. src/backend/app/config.py:
   - Clase de configuración usando pydantic-settings
   - Cargar variables desde .env
   - Variables: AZURE_OPENAI_ENDPOINT, AZURE_OPENAI_API_KEY, AZURE_OPENAI_DEPLOYMENT, AZURE_OPENAI_API_VERSION
   - Instancia global de configuración

2. src/backend/app/models/schemas.py con modelos Pydantic para:
   - FinancialProduct: id, name, type (cuenta/tarjeta/prestamo/inversion), description, interest_rate, monthly_fee, requirements (lista de strings)
   - ChatMessage: role (user/assistant/system), content
   - ChatRequest: message (str), history (lista opcional de ChatMessage)
   - ChatResponse: response (str), tokens_used (int opcional)
   - HealthResponse: status, version, service

```

### Paso 1.4: Implementar endpoint de salud

🤖 **PROMPT en Modo Agent:**

```
Crea el archivo src/backend/app/routers/health.py con:

1. Router de FastAPI con prefix "/api/health" y tag "Salud"
2. GET /api/health - Retorna estado del servicio
   - Respuesta: { "status": "saludable", "version": "1.0.0", "service": "Contoso Financial Services API" }
3. GET /api/health/ready - Verifica que el servicio esté listo
   - Incluye verificación básica del entorno (variables de configuración cargadas)
```

### Paso 1.5: Implementar endpoint de productos financieros

🤖 **PROMPT en Modo Agent:**

```
Crea el archivo src/backend/app/routers/products.py con:

1. Router de FastAPI con prefix "/api/products" y tag "Productos Financieros"

2. Datos de ejemplo hardcodeados con al menos 6 productos de Contoso:
   - Cuenta Contoso Plus (cuenta de ahorro, 4.5% anual)
   - Cuenta Contoso Empresarial (cuenta corriente empresarial)
   - Tarjeta Contoso Gold (tarjeta de crédito, tasa 28.9%)
   - Tarjeta Contoso Platinum (tarjeta premium, beneficios viajero)
   - Préstamo Contoso Personal (préstamo personal, tasa 12.5%)
   - Inversión Contoso Crecimiento (fondo de inversión, rendimiento 8.2%)

3. Endpoints:
   - GET /api/products - Lista todos los productos (con filtro opcional por tipo)
   - GET /api/products/{product_id} - Obtiene un producto por ID

```

### Paso 1.6: Implementar el archivo principal

🤖 **PROMPT en Modo Agent:**

```
Crea el archivo src/backend/app/main.py:

1. Aplicación FastAPI con:
   - Título: "Contoso Financial Services API"
   - Descripción: "API REST para el agente inteligente de servicios financieros de Contoso"
   - Versión: "1.0.0"

2. Configuración CORS para desarrollo:
   - Permitir orígenes: ["http://localhost:5173", "http://localhost:3000"]
   - Permitir métodos: todos
   - Permitir headers: todos

3. Incluir routers:
   - health
   - products
   - chat (lo crearemos después)

4. Evento de startup que imprima mensaje de bienvenida
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
@contoso-frontend Crea el archivo src/frontend/src/styles/contoso.css con los estilos principales:

1. Variables CSS con la paleta de colores corporativa Contoso
2. Reset CSS básico
3. Tipografía base con Segoe UI
4. Estilos para el layout principal:
   - Header corporativo con logo Contoso y navegación
   - Área de contenido principal
   - Footer con información de Contoso
5. Estilos para el componente de chat:
   - Contenedor del chat con altura fija y scroll
   - Burbujas de mensajes (usuario vs asistente)
   - Input de mensaje con botón de enviar
   - Indicador de escritura animado
   - Estado vacío (sin mensajes)
6. Estilos para tarjetas de productos financieros
7. Clases utilitarias para espaciado y layout
8. Estilos responsive (mobile, tablet, desktop)
```

### Paso 3.4: Crear componentes del chat

🤖 **PROMPT con Agente:**

```
@contoso-frontend Crea los siguientes componentes React en src/frontend/src/components/:

1. **Header.tsx**: Header corporativo de Contoso Financial Services
   - Logo (texto estilizado "CONTOSO")  
   - Título: "Asistente Virtual"
   - Fondo azul corporativo (#002050)

2. **MessageBubble.tsx**: Componente para cada mensaje en el chat
   - Props: content (string), isUser (boolean), timestamp (string)
   - Estilo diferente para usuario (azul, derecha) vs asistente (gris, izquierda)
   - Muestra "Tú" o "ContosoBot" como nombre del remitente
   - Formato de hora

3. **ChatInput.tsx**: Input para escribir mensajes
   - Campo de texto con placeholder "Escribe tu consulta financiera..."
   - Botón de enviar (ícono o texto "Enviar")
   - Deshabilitar mientras se espera respuesta
   - Enviar con Enter

4. **TypingIndicator.tsx**: Animación de "ContosoBot está escribiendo..."
   - Tres puntos animados
   - Se muestra solo mientras se espera respuesta

5. **ChatPanel.tsx**: Componente principal que integra todo el chat
   - Mantiene el estado del historial de mensajes
   - Llama a la API backend /api/chat
   - Auto-scroll al último mensaje
   - Estado de carga, error y vacío
   - Botón para limpiar conversación

Todos los componentes con TypeScript.
```

### Paso 3.5: Crear servicio HTTP para la API

🤖 **PROMPT con Agente:**

```
@contoso-frontend Crea el archivo src/frontend/src/services/api.ts con:

1. Configuración de axios con base URL: http://localhost:8000

2. Interfaces TypeScript:
   - ChatMessage { role: string; content: string }
   - ChatRequest { message: string; history?: ChatMessage[] }
   - ChatResponse { response: string; tokens_used?: number }
   - FinancialProduct { id, name, type, description, interest_rate, monthly_fee, requirements }

3. Funciones del servicio:
   - sendMessage(request: ChatRequest): Promise<ChatResponse>
   - getProducts(type?: string): Promise<FinancialProduct[]>
   - checkHealth(): Promise<boolean>

4. Manejo de errores con mensajes amigables
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
Containeriza mi aplicación backend en src/backend. Usa una imagen slim de Python, asegúrate de instalar las dependencias y expón el puerto 8000. Incluye un .dockerignore adecuado.
```

### Paso 4.2: Containerizar el frontend

🤖 **PROMPT en Modo Agent:**

```
Containeriza mi aplicación frontend en src/frontend. Usa multi-stage build: primero compila con Node.js y luego sirve con nginx en puerto 80. Incluye la configuración de nginx para SPA y un .dockerignore.
```

### Paso 4.3: Docker Compose

🤖 **PROMPT en Modo Agent:**

```
Crea un docker-compose.yml que levante el backend (puerto 8000) y el frontend (puerto 3000) juntos. El frontend depende del backend. Usa las variables de entorno del archivo .env del backend.
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
Crea el archivo infra/main.bicepparam con:

using './main.bicep'

param location = 'eastus2'
param environmentName = 'contoso-financial'
param imagenBackendTag = 'latest'
param imagenFrontendTag = 'latest'
```

### Paso 5.3: Desplegar infraestructura con Azure CLI

> 💡 **DEMOSTRACIÓN:** Desplegamos la infraestructura usando Azure CLI directamente en la terminal.

```bash
# 1. Iniciar sesión en Azure
az login

# 2. Seleccionar suscripción (si tienes varias)
az account set --subscription "TU_SUSCRIPCION"

# 3. Crear grupo de recursos
az group create \
  --name rg-contoso-financial \
  --location eastus2

# 4. Desplegar infraestructura con Bicep
az deployment group create \
  --resource-group rg-contoso-financial \
  --template-file infra/main.bicep \
  --parameters infra/main.bicepparam
```

### Paso 5.4: Subir imágenes a Azure Container Registry

```bash
# 1. Obtener nombre del ACR del deployment
ACR_NAME=$(az deployment group show \
  --resource-group rg-contoso-financial \
  --name main \
  --query properties.outputs.acrLoginServer.value -o tsv)

# 2. Login al ACR
az acr login --name $ACR_NAME

# 3. Construir y etiquetar imágenes
docker build -t $ACR_NAME/contoso-backend:v1 ./src/backend
docker build -t $ACR_NAME/contoso-frontend:v1 ./src/frontend

# 4. Subir imágenes al ACR
docker push $ACR_NAME/contoso-backend:v1
docker push $ACR_NAME/contoso-frontend:v1
```

### Paso 5.5: Configurar secrets de Azure OpenAI en Container Apps

```bash
# Obtener nombre de la Container App del backend
BACKEND_APP=$(az containerapp list \
  --resource-group rg-contoso-financial \
  --query "[?contains(name,'backend')].name" -o tsv)

# Configurar secrets
az containerapp secret set \
  --name $BACKEND_APP \
  --resource-group rg-contoso-financial \
  --secrets \
    azure-openai-endpoint="TU_ENDPOINT" \
    azure-openai-key="TU_API_KEY"
```

### Paso 5.6: Actualizar Container Apps con las imágenes

```bash
# Actualizar backend
az containerapp update \
  --name $BACKEND_APP \
  --resource-group rg-contoso-financial \
  --image $ACR_NAME/contoso-backend:v1

# Obtener y actualizar frontend
FRONTEND_APP=$(az containerapp list \
  --resource-group rg-contoso-financial \
  --query "[?contains(name,'frontend')].name" -o tsv)

az containerapp update \
  --name $FRONTEND_APP \
  --resource-group rg-contoso-financial \
  --image $ACR_NAME/contoso-frontend:v1
```

✅ **Verificar:**

```bash
# Obtener URLs de las aplicaciones
az containerapp show \
  --name $BACKEND_APP \
  --resource-group rg-contoso-financial \
  --query properties.configuration.ingress.fqdn -o tsv

az containerapp show \
  --name $FRONTEND_APP \
  --resource-group rg-contoso-financial \
  --query properties.configuration.ingress.fqdn -o tsv
```

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

📍 **En GitHub → Settings → Secrets and variables → Actions:**

| Secreto | Valor |
|---|---|
| `AZURE_CREDENTIALS` | JSON del Service Principal (ver comando abajo) |
| `ACR_LOGIN_SERVER` | URL del ACR (ej: contosofinancial.azurecr.io) |
| `ACR_USERNAME` | Username del ACR |
| `ACR_PASSWORD` | Password del ACR |
| `AZURE_OPENAI_ENDPOINT` | Endpoint de Azure OpenAI |
| `AZURE_OPENAI_API_KEY` | API Key de Azure OpenAI |
| `AZURE_OPENAI_DEPLOYMENT` | Nombre del deployment (ej: gpt-4o) |

```bash
# Crear Service Principal para GitHub Actions
az ad sp create-for-rbac \
  --name "sp-contoso-github-actions" \
  --role contributor \
  --scopes /subscriptions/TU_SUBSCRIPTION_ID/resourceGroups/rg-contoso-financial \
  --sdk-auth
```

### Paso 6.2: Crear pipeline CI/CD

🤖 **PROMPT en Modo Plan:**

```
Crea el archivo .github/workflows/ci-cd.yml con un pipeline completo:

1. **Trigger:**
   - Push a main y develop
   - Pull requests a main

2. **Job: test-backend**
   - Runs-on: ubuntu-latest
   - Steps:
     - Checkout código
     - Setup Python
     - Instalar dependencias de src/backend
     - Ejecutar linting con ruff (si disponible)
     - Ejecutar tests con pytest
   
3. **Job: test-frontend**
   - Runs-on: ubuntu-latest
   - Steps:
     - Checkout código
     - Setup Node.js
     - Instalar dependencias de src/frontend
     - Build del frontend (verifica que compila)

4. **Job: build-and-push** (solo en push a main)
   - Necesita: test-backend, test-frontend
   - Runs-on: ubuntu-latest
   - Steps:
     - Checkout código
     - Login a Azure Container Registry
     - Build y push imagen backend desde src/backend con tag: ${{ github.sha }}
     - Build y push imagen frontend desde src/frontend con tag: ${{ github.sha }}

5. **Job: deploy** (solo en push a main)
   - Necesita: build-and-push
   - Environment: produccion
   - Runs-on: ubuntu-latest
   - Steps:
     - Login a Azure con AZURE_CREDENTIALS
     - Actualizar Container App backend con nueva imagen
     - Actualizar Container App frontend con nueva imagen
     - Verificar health del backend desplegado
     - Comentar en commit con URLs de las apps

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
