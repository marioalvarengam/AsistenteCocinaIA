👩‍🍳 Asistente de Cocina impulsado por Gemini
==============================================

Este proyecto es una aplicación web _single-file_ (HTML, CSS y JavaScript en un solo archivo) diseñada para demostrar y probar las capacidades de las API de Google Gemini en un entorno local y seguro.

Está dirigido a desarrolladores que deseen experimentar con la generación de contenido (generateContent) y la síntesis de voz (TTS) utilizando su propia clave de API personal.

🚀 Funcionalidades
------------------

1.  **Generación de Recetas (Texto + Fundamentación):** Utiliza el modelo gemini-2.5-flash-preview-09-2025 para tomar una lista de ingredientes y generar una receta completa y creativa. Incluye la capacidad de **fundamentación (grounding)** a través de Google Search para asegurar la relevancia y actualidad de la información.
    
2.  **Síntesis de Voz (TTS):** Implementa el modelo gemini-2.5-flash-preview-tts para narrar las instrucciones de la receta, proporcionando una experiencia manos libres en la cocina.
    
3.  **Diseño Responsive:** Utiliza Tailwind CSS para asegurar una visualización óptima en dispositivos móviles y de escritorio.
    

🔑 Manejo de la Clave de API (Seguridad Crítica)
------------------------------------------------

**Advertencia:** Nunca debe almacenar su clave de API en texto plano ni subirla a un repositorio público (como GitHub). Una clave expuesta puede resultar en un uso no autorizado de su cuenta.

Este sitio web implementa un método seguro para la prueba local:

1.  **Entrada Enmascarada:** La aplicación expone un campo de entrada oculto () que permite al desarrollador pegar su clave de API de Gemini de forma manual.
    
2.  **Uso en Memoria:** La clave solo se lee en el momento de la llamada a la API y se mantiene exclusivamente en la memoria del navegador durante la sesión de uso. **La clave nunca se guarda en localStorage,** _**cookies**_**, o se almacena de forma persistente en el código fuente.**
    
3.  **Flexibilidad en Entornos de Google:** Si se ejecuta en un entorno que inyecta la clave automáticamente (como el entorno de desarrollo Canvas), el campo de entrada puede dejarse vacío, como se corrigió en el código.
    

🛠️ Configuración y Ejecución Local
-----------------------------------

Para ejecutar este proyecto en su máquina local, siga estos pasos:

### Requisitos

*   Una clave de API de Gemini válida, que puede obtener en [Google AI Studio](https://ai.google.dev/gemini-api/docs/api-key).
    
*   Un navegador web moderno (Chrome, Firefox, Edge, etc.).
    

### Pasos

1.  git clone cd
    
2.  open index.html
    
3.  **Insertar la Clave:** Si está ejecutando localmente o fuera de un entorno seguro, haga clic en "Configurar Clave de API" y pegue su clave personal en el campo enmascarado.
    
4.  **Probar:** Ingrese sus ingredientes y haga clic en "Generar Receta".
    

⚙️ Modelos de API Utilizados
----------------------------

| Tarea                       | Modelo                             | Uso                                                |
| --------------------------- | ---------------------------------- | -------------------------------------------------- |
| Generación de texto/Recetas | `gemini-2.5-flash-preview-09-2025` | Con `tools: google_search` para fundamentación.    |
| Síntesis de voz (TTS)       | `gemini-2.5-flash-preview-tts`     | Conversión de instrucciones de receta a audio PCM. |

_Desarrollado para pruebas de API de Gemini._
