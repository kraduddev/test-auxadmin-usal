# 🎓 Quiz de Repaso: Auxiliar Administrativo USAL

Este proyecto es una herramienta interactiva diseñada para el repaso de preguntas de exámenes reales (convocatorias 2014 y 2023) y normativa específica para la escala de **Auxiliar Administrativo de la Universidad de Salamanca**.

## 🚀 Características
- **Selector de tests**: Al cargar la página se muestra una pantalla inicial para elegir entre los tests disponibles.
- **Formato Flashcards**: Sistema de pregunta-respuesta con retroalimentación inmediata.
- **Justificación Legal**: Cada respuesta incluye una explicación basada en el artículo correspondiente de la ley o estatuto.
- **Diseño Adaptativo**: Interfaz limpia, optimizada para dispositivos móviles y escritorio.
- **Sin Dependencias**: Escrito en HTML, CSS y JavaScript puro (Vanilla JS), lo que facilita su despliegue en cualquier servidor estático.
- **Preguntas en JSON**: El banco de preguntas está externalizado en ficheros `.json` independientes, facilitando su mantenimiento y ampliación.

## 📂 Estructura de ficheros
```
index.html          → Interfaz principal con el selector y el motor del quiz
questions.json      → Banco de preguntas del Test General (preguntas mixtas)
estatutos.json      → Banco de preguntas: Estatutos de la USAL
ebep.json           → Banco de preguntas: EBEP
39_2015.json        → Banco de preguntas: Ley 39/2015
40_2015.json        → Banco de preguntas: Ley 40/2015
transparencia.json  → Banco de preguntas: Ley 19/2013 de Transparencia
```

## 🧪 Tests disponibles

### 🏛️ Estatutos USAL (`estatutos.json`)
Estructura, órganos colegiados y unipersonales, procesos electorales, programación plurianual y comunidad universitaria.

### 👔 EBEP (`ebep.json`)
Estatuto Básico del Empleado Público: derechos, deberes, situaciones administrativas, régimen disciplinario y carrera profesional.

### 📋 Ley 39/2015 (`39_2015.json`)
Procedimiento Administrativo Común: iniciación, instrucción, terminación, notificaciones, plazos y silencio administrativo.

### ⚖️ Ley 40/2015 (`40_2015.json`)
Régimen Jurídico del Sector Público: abstención, órganos colegiados, competencias, responsabilidad patrimonial y prescripción.

### 🔍 Ley de Transparencia (`transparencia.json`)
Ley 19/2013: ámbito subjetivo, publicidad activa, derecho de acceso, Consejo de Transparencia e infracciones de Buen Gobierno.

### 📚 Test General (`questions.json`)
Preguntas mixtas que combinan normativa de todas las materias anteriores.

## 🛠️ Instalación y Despliegue

### Local (requiere servidor HTTP)
> ⚠️ El `fetch` de los ficheros JSON no funciona con el protocolo `file://`. Usa un servidor local:

```bash
python3 -m http.server
```
Luego accede a `http://localhost:8000`.

### Despliegue en Servidor (GitHub Pages / Vercel)
1. Sube `index.html`, `questions.json`, `estatutos.json`, `ebep.json`, `39_2015.json`, `40_2015.json` y `transparencia.json` al repositorio.
2. Activa la opción de **Static Pages** (en GitHub: *Settings > Pages*).
3. El sitio estará disponible en la URL proporcionada por la plataforma.

## 📝 Notas sobre el Contenido
Las preguntas han sido mapeadas directamente desde exámenes oficiales:
* **Examen 2023**: Preguntas sobre voto ponderado, Unidad de Igualdad y leyes 39/40.
* **Examen 2014**: Preguntas sobre el Claustro de Doctores y fines de la Universidad.

---
*Desarrollado como herramienta de apoyo al estudio para opositores de la USAL.*
