# satellite_passes

# Cálculo de Pases de Satélites

Este repositorio contiene un **script en Python** que:
1. Descarga los TLE (Two-Line Elements) desde [Celestrak](https://celestrak.org).
2. Calcula los **próximos pases** de distintos satélites en las ventanas horarias definidas (por defecto, los **próximos 3 lunes** de 18:00 a 21:00 hora local).
3. Filtra solo aquellos con **elevación máxima** dentro de un rango determinado.
4. Muestra datos relevantes, incluyendo frecuencia, modo de transmisión e inclinación orbital.

## Características principales

- **Consulta automática** de TLE a través de `requests`.
- Cálculos con [**Skyfield**](https://rhodesmill.org/skyfield/) (posiciones satelitales y eventos de paso).
- Manejo de **fechas y zonas horarias** con [**pytz**](https://pypi.org/project/pytz/).
- Filtro por **elevación máxima** y **ventanas horarias** específicas.
- Diccionario `SAT_INFO` con información adicional (descripción, frecuencias, modos).

---

## Requisitos

- **Python 3.7+**  
- [**requests**](https://pypi.org/project/requests/)  
- [**skyfield**](https://pypi.org/project/skyfield/)  
- [**pytz**](https://pypi.org/project/pytz/)  

Puedes instalar estas dependencias manualmente o usar un `requirements.txt` (si lo proporcionas) con:
```bash
pip install -r requirements.txt
