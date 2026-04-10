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
questions.json      → Banco de preguntas del Test General
transparencia.json  → Banco de preguntas del Test de Transparencia
```

## 🧪 Tests disponibles

### 📚 Test General (`questions.json`)
Cubre los siguientes bloques normativos:
* **Estatutos de la Universidad de Salamanca**: Regulación de órganos, procesos electorales y programación plurianual.
* **Ley 39/2015**: Procedimiento Administrativo Común (notificaciones, plazos, silencio administrativo).
* **Ley 40/2015**: Régimen Jurídico del Sector Público (abstención, órganos colegiados, prescripción).
* **Código Ético USAL**: Denuncias y principios de conducta.

### 🔍 Test de Transparencia (`transparencia.json`)
Cubre en profundidad la **Ley 19/2013 de Transparencia, Acceso a la Información Pública y Buen Gobierno**:
* Ámbito subjetivo y publicidad activa (Arts. 1–10).
* Derecho de acceso: titulares, límites, procedimiento y silencio administrativo (Arts. 12–22).
* Reclamaciones ante el Consejo de Transparencia y Buen Gobierno (Art. 24).
* Infracciones y sanciones de Buen Gobierno (Arts. 26–32).
* Consejo de Transparencia: composición, funciones y nombramiento (Arts. 33–38).

## 🛠️ Instalación y Despliegue

### Local (requiere servidor HTTP)
> ⚠️ El `fetch` de los ficheros JSON no funciona con el protocolo `file://`. Usa un servidor local:

```bash
python3 -m http.server
```
Luego accede a `http://localhost:8000`.

### Despliegue en Servidor (GitHub Pages / Vercel)
1. Sube `index.html`, `questions.json` y `transparencia.json` al repositorio.
2. Activa la opción de **Static Pages** (en GitHub: *Settings > Pages*).
3. El sitio estará disponible en la URL proporcionada por la plataforma.

## 📝 Notas sobre el Contenido
Las preguntas han sido mapeadas directamente desde exámenes oficiales:
* **Examen 2023**: Preguntas sobre voto ponderado, Unidad de Igualdad y leyes 39/40.
* **Examen 2014**: Preguntas sobre el Claustro de Doctores y fines de la Universidad.

---
*Desarrollado como herramienta de apoyo al estudio para opositores de la USAL.*
