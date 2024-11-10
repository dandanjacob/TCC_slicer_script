# Slicing and 3D Model Reconstruction

Este repositório contém a implementação de um método para fatiamento de objetos tridimensionais e extração de nuvens de pontos a partir de coleções de imagens paralelas. O projeto faz parte do Trabalho de Conclusão de Curso (TCC) intitulado **"Um estudo sobre fatiamento e reconstrução de modelos 3D"**, desenvolvido por Daniel Jacob Tonn na FGV/EMAp.

## 📖 Overview

### Key Features
- Fatiamento automatizado de modelos 3D em seções paralelas utilizando Blender Python API (`bpy`).
- Detecção de bordas em fatias 2D usando o filtro de Sobel.
- Construção de nuvens de pontos tridimensionais salvas no formato `.ply`.
- Visualização e manipulação de nuvens de pontos com MeshLab.

---

## 📂 Repository Structure

- `notebooks/automatic_slicer.ipynb`: Notebook Jupyter com a implementação Python para fatiamento e extração de nuvens de pontos.
- `data/`: Diretório para armazenar nuvens de pontos geradas e objetos de teste.
- `results/`: Pasta contendo exemplos de saída, incluindo nuvens de pontos e modelos reconstruídos.
- `docs/`: Documentação adicional e materiais de pesquisa relacionados.

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
   - Carregue seu modelo 3D no Blender.
   - Certifique-se de que está escalado e posicionado corretamente para o fatiamento.

2. **Run the Slicing Script:**
   - Abra `automatic_slicer.ipynb` e configure os parâmetros de fatiamento (e.g., espaçamento entre planos, diretório de saída).
   - Execute o script para gerar fatias 2D e extrair a nuvem de pontos.

3. **Visualize Results:**
   - Abra o arquivo `.ply` gerado no MeshLab para visualizar a nuvem de pontos reconstruída.

---

## 📊 Results and Comparisons

O método foi testado em diversos modelos, como:
- Stanford Bunny
- Teapot
- Cow

O projeto destaca-se pela precisão na detecção de bordas e reconstrução, mas apresenta limitações na captura de variações bruscas de superfície e cavidades internas.

---

## 🛠️ Future Work

- Integrar orientações adicionais de fatiamento (e.g., sagital, coronal) para reconstruções mais abrangentes.
- Explorar técnicas avançadas de interpolação e aprendizado de máquina para melhorar a detecção de bordas e a qualidade da superfície.

---

## 📝 Citation

Se você usar este código ou método em seu trabalho, por favor, cite:

