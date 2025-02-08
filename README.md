# Investigación e Implementación de una GigaGAN

<p align="center">
  <img src="https://github.com/warc0s/GigaGAN_Research/blob/main/logo_gigaGAN.png?raw=true" alt="GigaGAN Research" width="95%">
</p>

## Descripción General
Este repositorio presenta una exploración exhaustiva que abarca tanto la investigación teórica como una implementación práctica completa de una **GigaGAN**. El proyecto culmina con una GigaGAN para la generación de imágenes de Pastores Alemanes, utilizando un dataset sintético generado localmente. Puedes consultar el detalle teórico sobre GigaGAN en [investigacion.md](investigacion.md) y la implementación práctica en el [cuaderno Jupyter](GigaGAN_GS.ipynb).

## 📁 Estructura del Repositorio
- `investigacion.md` - Investigación técnica detallada sobre GigaGAN
- `GigaGAN_GS.ipynb` - Cuaderno Jupyter con la implementación completa, proceso de entrenamiento y resultados 
- `checkpoints/` - Checkpoints del modelo guardados cada 5 épocas (hasta la época 100)
- `epoch_images/` - Visualización del progreso de entrenamiento (muestras 3x3) guardadas cada 5 épocas

## 🔍 Detalles de la Implementación Práctica
 
### Generación del Dataset
- **Origen**: Dataset sintético generado localmente mediante **Flux Schnell** (una versión destilada y más eficiente de Flux Dev)
- **Especificaciones**:
  - 5,000 imágenes en resolución 256x256
  - Escenarios diversos y realistas (parques, entornos urbanos, fondos nevados, etc.)
  - Tiempo de generación: ~2 horas en mi RTX 3090
- **Disponibilidad del dataset**: Tras completar la generación del dataset, decidí compartirlo con la comunidad subiéndolo a Kaggle para que otros investigadores y entusiastas puedan beneficiarse de él. Está disponible en [este enlace](https://www.kaggle.com/datasets/warc0s/german-shepherd)

### Proceso del Entrenamiento
- **Preprocesamiento**: Redimensionado a 128x128 para acelerar el entrenamiento
- **Duración del entrenamiento**: 100 épocas (~18 horas en mi RTX 3090)
- **Monitorización**:
  - Checkpoints sistemáticamente guardados cada 5 épocas (archivos `.pth`)
  - Visualización detallada del progreso mediante muestras 3x3

### Evolución del Entrenamiento
![Training GIF](https://github.com/warc0s/GigaGAN_Research/blob/main/epoch_images/output.gif?raw=true)

## 📝 Investigación Teórica
Para terminar, recuerdo que el archivo [investigacion.md](investigacion.md) contiene un análisis en profundidad de la arquitectura GigaGAN, incluyendo sus autores, tecnologías clave, innovaciones principales y comparativas con otras GANs similares así como modelos de difusión.

## 📄 Licencia
Este proyecto está bajo la Licencia MIT.
