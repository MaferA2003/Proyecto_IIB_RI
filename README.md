# Proyecto_IIB_RI
# Descripción
Este sistema combina técnicas de recuperación multimodal y generación aumentada por recuperación (RAG) para crear una experiencia de búsqueda inteligente de productos de moda. 
El sistema puede procesar tanto consultas de texto como imágenes para encontrar productos similares y generar descripciones detalladas de los mismos.
# Funcionalidades Principales
Búsqueda Multimodal: Busca productos usando imágenes o descripciones de texto
Generación RAG: Utiliza Gemini para generar descripciones detalladas de productos
Indexación Vectorial: Usa FAISS para búsquedas eficientes en espacios vectoriales
Interfaz Visual: Interfaz web interactiva con Gradio
Embeddings CLIP: Codifica imágenes y texto en un espacio vectorial común
# Descripción del Corpus
Para el desarrollo del presente proyecto se utilizó un conjunto de datos extraído de la plataforma Kaggle, específicamente del dataset titulado “Fashion Product Images Dataset” publicado por Param Aggarwal.
Este corpus proviene del sector del comercio electrónico y está compuesto por una amplia colección de productos de moda. 
# Contenido del Corpus:
Imágenes Profesionales:
- Fotografías de artículos de ropa
- Fondo neutro y iluminación uniforme
- Cada producto identificado por un ID único (ej: 42431)
- Acceso directo: images/42431.jpg
# Metadatos Estructurados:
- Múltiples atributos categóricos ingresados manualmente durante la catalogación
- Mapeo completo de productos en styles.csv
- Categorías clave expuestas para facilitar el desarrollo
- Información jerárquica: masterCategory → subCategory → articleType
# Texto Descriptivo:
- Comentarios detallados sobre las características del producto
- Descripciones que complementan la información visual
- Nombres de productos descriptivos y comerciales
# Prerequisitos
- Python 3.7+
- CUDA (opcional, para aceleración GPU)
- Cuenta de Google AI Studio para API key de Gemini
# Instalación de dependencias
pip install google-generativeai gradio torch torchvision transformers
pip install sentence-transformers faiss-cpu pandas pillow matplotlib tqdm
pip install kaggle  # Para descargar el dataset
# Descargar dataset de Kaggle
!kaggle datasets download -d paramaggarwal/fashion-product-images-small
# Interfaz Web
La interfaz permite:
- Subir imágenes de productos
- Escribir consultas de texto
- Ajustar número de resultados
- Ver productos similares
- Leer descripciones generadas por IA
