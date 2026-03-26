# 🏥 Sistema de Triaje y Llamada de Pacientes
Proyecto de prueba para sistema de gestión hospitalaria de código abierto diseñado para automatizar la clasificación de urgencias (Triage) y la comunicación visual con la sala de espera mediante una API REST local.


# 🚀 Características principales
**Triage Digital:** Clasificación de pacientes basada en protocolos estándar.

**Pantalla de Guardia:** Comunicación en tiempo real entre el puesto de enfermería y la sala de espera vía API.

**Base de Datos Local:** Almacenamiento en SQLite (sin necesidad de servidores externos).

**Reportes Automáticos:** Exportación de datos diarios a hojas de cálculo y reportes en PDF.

**Privacidad:** Funcionamiento 100% en red local (LAN) para proteger datos sensibles.


# 🛠️ Stack Tecnológico
***Lenguaje:*** Python 3.x

***Backend / API:*** [FastAPI](https://pypi.org/project/fastapi/) + [Uvicorn](https://pypi.org/project/uvicorn/)

***Base de Datos:*** [SQLite](https://sqlite.org/)

***Procesamiento de Datos:*** [Pandas](https://pypi.org/project/pandas/)

***Generación de Reportes:*** [FPDF2](https://pypi.org/project/fpdf2/) (PDF) y [ReportLab](https://pypi.org/project/reportlab/) (Excel)

---

# ⚙️ Configuración e Instalación
## Clonar el repositorio:

```Bash
git clone https://github.com/tu-usuario/sistema-triage-hospital.git
cd sistema-triage-hospital
```

## Iniciar el Servidor:

```Bash
uvicorn main:app --host 0.0.0.0 --port 8000
```

`Nota: El host 0.0.0.0 permite conexiones desde otras computadoras en la misma red.`

## Acceso a la Interfaz:

🩹 Enfermería: Abrir el cliente de ingreso de datos.

🖥️ Pantalla Sala de Espera: Acceder a la URL del servidor (ej. `http://192.168.1.50:8000/pantalla`).

---

# 📊 Estructura del Proyecto
```text
    Sistema-Triage/
    ├── app/
    │   ├── main.py          # Servidor FastAPI y Rutas
    │   ├── database.py      # Configuración SQLite
    │   └── reports.py       # Lógica de Pandas y FPDF2
    ├── data/
    │   └── hospital.db      # Base de datos (Local)
    ├── reports/
    │   ├── diario.xlsx      # Exportación Excel
    │   └── diario.pdf       # Reporte formal
    ├── .gitignore           # Archivos ignorados por Git
    ├── requirements.txt     # Librerías necesarias
    └── README.md            # Documentación
```

# 📑 Uso de Reportes
Para generar el cierre del día, el sistema procesa la base de datos y genera dos archivos:
| Archivo | Función |
|:---:|:---:|
| `reporte_diario.xlsx` | Resumen tabular para análisis administrativo.|
| `reporte_diario.pdf` | Documento formal con encabezado y firmas.|


# 🔒 Seguridad y Privacidad
Este sistema cumple con el manejo local de datos:

✅ No requiere conexión a internet para funcionar.

✅ Los datos se almacenan exclusivamente en el disco duro local.

✅ Se recomienda realizar copias de seguridad diarias del archivo hospital.db.

# 📄 Licencia
Este proyecto es de código abierto bajo la licencia MIT.
