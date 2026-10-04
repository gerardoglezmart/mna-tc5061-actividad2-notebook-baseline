# Actividad 2: Dataset y notebook baseline con MLflow

Repositorio: https://github.com/gerardoglezmart/mna-tc5061-actividad2-notebook-baseline

TC5061.10, Operaciones de aprendizaje automático (MLOps). Maestría en Inteligencia Artificial
Aplicada.

Entregable: `TC5061_Notebook_Baseline_GonzalezMartinezGerardo.ipynb`

Dataset: Wine Quality tinto del UCI Machine Learning Repository. Problema de clasificación
binaria, un vino se considera bueno si su calidad es 7 u 8.

## Cómo ejecutarlo

```bash
source ../../semana1/mna-tc5061-actividad1-deuda-tecnica-mlflow/mlops-env-wk1/bin/activate
pip install mlflow scikit-learn pandas matplotlib jupyter
mlflow ui --port 5000
```

Con el servidor arriba, en otra terminal:

```bash
jupyter notebook TC5061_Notebook_Baseline_GonzalezMartinezGerardo.ipynb
```

## Contenido

| Archivo | Descripción |
|---|---|
| `TC5061_Notebook_Baseline_GonzalezMartinezGerardo.ipynb` | Notebook ejecutado, con las siete secciones y las capturas incrustadas |
| `data/winequality-red.csv` | Copia local del dataset, 1,599 registros |
| `capturas/01_mlflow_experimento.png` | Las dos corridas en la MLflow UI, con parámetros y métricas |
| `capturas/02_terminal_mlflow_ui.png` | La consola con el servidor de tracking arrancando |
| `mlflow.db` y `mlartifacts/` | Base de tracking y artefactos de las corridas |

## Resultados

| Modelo | accuracy | F1 | ROC-AUC |
|---|---|---|---|
| DummyClassifier | 0.864 | 0.000 | 0.500 |
| LogisticRegression | 0.875 | 0.346 | 0.886 |

El accuracy del modelo trivial parece alto solo porque el 86 % de los vinos no son buenos. Por
eso la comparación se hace con F1 y ROC-AUC.

## Declaración de uso de herramientas de inteligencia artificial

En esta entrega se utilizó Claude Code de Anthropic, con el modelo Claude Opus 5.5, para la
generación parcial de código, orientada a mejorar el código propuesto y a plantear
alternativas basadas en decisiones de optimización.

Anthropic. (2026). Claude Code (Claude Opus 5.5) [Modelo de lenguaje grande], utilizado para
generación parcial de código, mejora del código propuesto y alternativas de optimización.
https://claude.com/claude-code
