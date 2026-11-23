# diagnostico-falhas-rolamento-crwu
Diagnóstico de falhas em rolamentos por vibração (FFT, envelope e machine learning) com o dataset CWRU. Python.

markdown
# Diagnóstico de falhas em rolamentos por vibração (CWRU)

Classificação de 10 condições de rolamento (sadio e falhas de pista interna, pista externa e esfera, em 3 severidades) com FFT, espectro de envelope e indicadores estatísticos.

## Resultados (carga 1 hp, 48 kHz, teste temporal)
- Energia por banda espectral: 98,7–99,7% de acurácia
- Indicadores no tempo (RMS, curtose, fator de crista): 87–91%
- Espectro de envelope: ~80% (funciona bem só para pista interna)

## Limitações
Um único registro por classe; sem validação em outras cargas ou máquinas. Os ~99% não devem ser extrapolados para campo.

## Como rodar
1. Baixe os dados no CWRU Bearing Data Center e extraia em `raw/`.
2. `pip install -r requirements.txt`
3. Abra `estudo_cwru.ipynb`.
