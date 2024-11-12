# Slicing and 3D Model Reconstruction

Este repositório contém a implementação de um método para fatiamento de objetos tridimensionais e extração de nuvens de pontos a partir de coleções de imagens paralelas. O projeto faz parte do Trabalho de Conclusão de Curso (TCC) intitulado **"Um estudo sobre fatiamento e reconstrução de modelos 3D"**, desenvolvido por Daniel Jacob Tonn na FGV/EMAp.
Em virtude das limitações de espaço, apenas um dos testes presentes no arquivo pdf se encontram disponíveis no repositório. É posível rodar localmente com os mesmos arquivos testados afim de averiguar os resultados.

## 📖 Overview

### Key Features
- Fatiamento automatizado de modelos 3D em seções paralelas utilizando Blender Python API (`bpy`).
- Detecção de bordas em fatias 2D usando o filtro de Sobel.
- Construção de nuvens de pontos tridimensionais salvas no formato `.ply`.
- Visualização e manipulação de nuvens de pontos com MeshLab.

---

## 📂 Repository Structure

- `automatic_slicer.ipynb`: Notebook Jupyter com a implementação Python para fatiamento e extração de nuvens de pontos.
- `blender_arquives/`: Diretório para armazenar objetos 3D do blender.
- `planes_intersections/`: Onde estão as pastas que contém as seções fatiadas dos objetos.
- `meshlab_arquives/`: Arquivos `.ply` contendo nuvem de pontos.

---

## 🔧 Requirements

- Python 3.10 ou mais recente
- Blender 3.x com suporte à API Python habilitado
- MeshLab
- Bibliotecas Python necessárias: 
  - `numpy`
  - `opencv-python`
  - `matplotlib`
  - `plyfile`

---

## 🚀 How to Use

1. **Prepare Your 3D Model:**
   - Tenha seu modelo 3D originário do blender.
   - Certifique-se de que está escalado e posicionado corretamente para o fatiamento.

2. **Run the Slicing Script:**
   - Abra `automatic_slicer.ipynb` e configure os parâmetros de fatiamento (e.g., espaçamento entre planos, diretório de saída e nome do objeto).
   - Importante: o nome do objeto e o nome do arquivo devem ser os mesmos.
   - Execute o script para gerar fatias 2D e extrair a nuvem de pontos.

3. **Visualize Results:**
   - Abra o arquivo `.ply` gerado no MeshLab para visualizar a nuvem de pontos reconstruída.

---

## 📊 Results and Comparisons

O método foi testado em alguns repositórios, como:
- Stanford Bunny
- Teapot
- Cow
  
Em virtude da limitação de armazenamento do github, somente o teste em Bunny Stanford foi enviado.
---

## 🛠️ Future Work

- Integrar orientações adicionais de fatiamento (e.g., sagital, coronal) para reconstruções mais abrangentes.
- Explorar técnicas avançadas de interpolação e aprendizado de máquina para melhorar a detecção de bordas e a qualidade da superfície.


