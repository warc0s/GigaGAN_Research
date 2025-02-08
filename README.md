# Investigación sobre GigaGAN

Este repositorio contiene tanto la documentación de la investigación sobre **GigaGAN** como una implementación práctica de la misma.  
Puedes consultar el detalle teórico en [investigacion.md](investigacion.md) y la parte práctica en el cuaderno Jupyter **GigaGAN_GS.ipyn**.

---

## Contenido del Repositorio

- **README.md**: Descripción general del repositorio y resumen de la implementación práctica.
- **investigacion.md**: Documento con la investigación detallada sobre GigaGAN.
- **GigaGAN_GS.ipyn**: Cuaderno Jupyter donde se ha entrenado la GigaGAN.
- **checkpoints/**: Carpeta que contiene los checkpoints (.pth) de la GAN cada 5 épocas (hasta la época 100).
- **epoch_images/**: Carpeta con imágenes de muestra (en formato 3x3) cada 5 épocas para visualizar la evolución del entrenamiento.

---

## Ejemplo Práctico: Generación de Imágenes Realistas de Pastores Alemanes 🐕

La idea es generar imágenes realistas de **pastores alemanes**. A continuación, explico brevemente el proceso:

- **Dataset Sintético:**  
  - Para contar con un dataset grande, se generó uno sintético usando **Flux Schell** *(una versión destilada de Flux Dev, mucho más veloz)*.  
  - Se crearon **5000 imágenes** de **256x256**.  
  - Cada lote de 100 imágenes contenía escenarios diferentes (parque, ciudad, fondo nevado, etc.) y cada lote tardó aproximadamente **2 minutos** en generarse.  
  - En total, la generación del dataset tomó cerca de **2 horas** utilizando mi RTX 3090.  
  - El dataset se ha subido a Kaggle y está disponible en [este enlace](https://www.kaggle.com/datasets/warc0s/german-shepherd).

- **Preprocesado:**  
  Las imágenes se pasaron a **128x128** para facilitar y acelerar el entrenamiento (generarlas directamente en 128x128 reducía demasiado la calidad).

- **Entrenamiento:**  
  El entrenamiento se realizó durante **100 épocas**, con una duración aproximada de **18 horas** en mi RTX 3090 de forma local.

- **Resultados:**  
  - **Checkpoints:** Se han guardado archivos `.pth` cada 5 épocas (ubicados en la carpeta `checkpoints`).
  - **Imágenes de Evolución:** Se han guardado imágenes en formato 3x3 cada 5 épocas en la carpeta `epoch_images`.

---

### Evolución del Entrenamiento

*(Insertar GIF aquí con la evolución de las imágenes durante el entrenamiento)*  
**[insertar gif aquí]** 📈

(en cuanto se entrene del todo lo subo)
