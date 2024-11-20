# Agents_LangChain_2_IA: Sistema de Análisis y Generación de QR
Esta aplicación implementa un sistema inteligente de agentes utilizando LangChain y GPT-4 para analizar datos de episodios de series y generar códigos QR. El sistema incluye agentes especializados para ejecutar código Python y analizar archivos CSV.

## Requisitos Previos
- Python 3.8 o superior
- Cuenta de OpenAI con clave API
- Instalación de paquetes necesarios (ver requirements.txt)
## Instalación

1. Clonar el repositorio:
```bash
git clone https://github.com/Maria-Villafuerte/Agents_LangChain_2_IA
cd Agents_LangChain_2_IA
python agent.py
```

2. Crear y activar un entorno virtual:
```bash
python -m venv myenv
source myenv/bin/activate  # En Windows: myenv\Scripts\activate
```

3. Instalar las dependencias:
```bash
pip install -r .\requirements.txt
```

4. Configurar las variables de entorno:
   - Crear un archivo `.env` en el directorio raíz
   - Agregar la clave API de OpenAI:
```
OPENAI_API_KEY=tu-clave-api
```

## Estructura del Proyecto
```
├── agents.py         # Implementación principal de los agentes
├── main.py          # Punto de entrada alternativo
├── episode_info.csv # Datos de episodios
├── .env            # Variables de entorno
└── .gitignore      # Archivos ignorados por git
```

## Características Principales

### 1. Agente Python
- Ejecuta código Python dinámicamente
- Genera códigos QR
- Depura y corrige errores automáticamente
- Acceso a REPL de Python

### 2. Agente CSV
- Analiza datos del archivo episode_info.csv
- Ejecuta cálculos con pandas
- Responde consultas sobre episodios

### 3. Agente Principal
- Coordina los agentes especializados
- Selecciona la herramienta más apropiada
- Procesa lenguaje natural

## Uso

### Ejecutar la Aplicación
```bash
python agents.py
```

### Ejemplos de Consultas

1. Análisis de episodios:
```bash
grand_agent_executor.invoke({
    "input": "¿Qué temporada tiene más episodios?"
})
```

2. Generación de códigos QR:
```bash
grand_agent_executor.invoke({
    "input": "Generar y guardar 15 códigos QR que apunten a www.google.com"
})
```

