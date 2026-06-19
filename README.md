# Bot de Mesa de Ayuda Técnica
### Trabajo Práctico Integrador — Organización Empresarial
**UTN — Tecnicatura Universitaria en Programación (TUP)**

---

## Descripción
Simulador de chatbot que automatiza el proceso de Mesa de Ayuda 
Técnica (Soporte IT Nivel 1). El bot recibe el problema del usuario, 
consulta una base de conocimiento y resuelve automáticamente o 
deriva a un técnico de Nivel 2.

## Tecnologías utilizadas
- Python 3.10+
- openpyxl (lectura/escritura de Excel)
- Simulación en consola (sin API externa)

## Estructura del proyecto
mesa-ayuda-bot/

├── bot.py                        → código principal del bot

├── data/

│   └── base_datos_mesa_ayuda.xlsx → base de datos simulada

└── docs/

├── BPMN_AS-IS_MesaAyuda.png  → diagrama proceso manual

└── BPMN_TO-BE_MesaAyuda.png  → diagrama proceso con bot

## Cómo ejecutarlo
1. Instalar Python 3.10 o superior
2. Instalar la dependencia:
pip install openpyxl
3. Clonar el repositorio o descargar los archivos
4. Ejecutar desde la terminal:
python bot.py

## Comandos del bot
| Comando | Acción |
|---|---|
| `/start` | Inicia la conversación |
| `/salir` | Cancela la sesión actual |

## Flujo del proceso
1. Usuario ingresa legajo y categoría del problema
2. Bot busca solución en la base de conocimiento (FAQ)
3. Si encuentra solución → la envía y consulta si se resolvió
4. Si no encuentra o el usuario dice "no" → genera ticket y deriva

## Autor
Agustín Ezequiel Fernández — Cohorte Marzo 2026
Paso 5 — Verificar que quedó bien
Al terminar, tu repositorio tiene que verse así desde la página principal:
mesa-ayuda-bot/
├── README.md          ← se ve automáticamente en la página
├── bot.py
├── data/
│   └── base_datos_mesa_ayuda.xlsx
└── docs/
    ├── BPMN_AS-IS_MesaAyuda.png
    └── BPMN_TO-BE_MesaAyuda.png




    
