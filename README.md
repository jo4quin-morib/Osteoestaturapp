# OsteoEstatura

**Estimación forense de estatura desde mediciones de huesos largos mediante Bayesian Model Averaging y corrección ecogeográfica BGLMM.**

Construido para la tesis *Análisis de Sesgo en Estimación de Estatura Esquelética* (Moreno Ibarra, 2026) — Universidad de Concepción, Antropología Forense.

📄 **DOI:** [10.5281/zenodo.18893064](https://doi.org/10.5281/zenodo.18893064)

---

## 🚀 Uso en GitHub Pages

### Paso 1 — Subir el archivo

```bash
git clone https://github.com/TU-USUARIO/osteoestatura
cd osteoestatura
# Copia osteoestatura.html aquí
git add osteoestatura.html README.md
git commit -m "Add OsteoEstatura app"
git push
```

### Paso 2 — Activar GitHub Pages

1. Ve a tu repositorio en GitHub
2. **Settings → Pages**
3. En *Source*, selecciona **Deploy from a branch**
4. Branch: `main` | Folder: `/ (root)`
5. Haz clic en **Save**

Después de ~2 minutos, la app estará disponible en:
```
https://TU-USUARIO.github.io/osteoestatura/osteoestatura.html
```

---

## ✦ Informe Pericial IA

La función de informe pericial llama directamente a la API de Anthropic desde tu navegador.  
Al hacer clic en **✦ INFORME PERICIAL IA**, la app te pedirá tu API key si aún no la has ingresado.

- La clave se guarda **solo en tu navegador** (localStorage), nunca se envía a ningún servidor externo
- Obtén una clave en [console.anthropic.com/keys](https://console.anthropic.com/keys)
- Puedes cambiarla en cualquier momento: borra el ítem `osteo_api_key` de tu localStorage

---

## Módulos

| Módulo | Descripción |
|--------|-------------|
| **Estimador** | Ingresa mediciones de huesos, sexo y origen poblacional. Calcula 11 fórmulas clásicas + BMA + corrección ecogeográfica BGLMM |
| **Análisis Estadístico** | Estadísticas descriptivas, LMM, BGLMM, Bland-Altman, Games-Howell, XGBoost |
| **ML Lab** | Constructor OLS sobre el dataset Goldman (n=1,537). Filtros por sexo y país |

---

## Métodos implementados

| Autor(es) | Año | Huesos | Población |
|-----------|-----|--------|-----------|
| Pearson | 1899 | F, T, H, R | Europa |
| Telkkä | 1950 | F, T, H, R | Europa / Finlandia |
| Trotter & Gleser | 1952 | F | Europa / USA |
| Trotter & Gleser | 1958 | F | Afrodescendiente |
| Genovés | 1967 | F, T | Mesoamérica |
| Del Ángel & Cisneros | 2004 | F, T, H, R | México |
| Béguelin | 2011 | F, T, H, R | Patagonia |
| Belmonte et al. | 2011 | T | España (♀) |
| Ross & Manneschi | 2011 | F, T, H | Chile |
| Abarca | 2013 | F | Chile |
| Menéndez et al. | 2018 | F, T, H | Patagonia / Argentina |

---

## Datos

Basado en la **Goldman Skeletal Collection** — base de datos osteométrica de acceso abierto compilada por Dr. Benjamin M. Auerbach (University of Tennessee).

- n = 1,538 individuos · 15 países · esqueletos adultos
- Huesos: fémur (p_LMF), tibia (p_LMT), húmero (p_LMH), radio (p_LMR)

---

## Cita

```
Moreno Ibarra, J. (2026). Análisis de sesgo en estimación de estatura esquelética:
Estudio comparativo de métodos osteométricos usando el dataset Goldman.
Universidad de Concepción. DOI: 10.5281/zenodo.18893064
```

---

## Licencia

Herramienta provista para uso académico e investigación.  
Los datos Goldman Skeletal Collection son cortesía del Dr. Benjamin M. Auerbach.
