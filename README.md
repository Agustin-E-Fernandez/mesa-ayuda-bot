# Bot de Mesa de Ayuda Técnica
### Trabajo Práctico Integrador — Organización Empresarial
**UTN — Tecnicatura Universitaria en Programación (TUP)**

---

## Descripción
Simulador de chatbot que automatiza el proceso de Mesa de Ayuda
Técnica (Soporte IT Nivel 1). El bot recibe el problema del usuario,
consulta una base de conocimiento (FAQ) y resuelve automáticamente
o deriva el caso a un técnico de Nivel 2, registrando todo en una
base de datos simulada en Excel.

## Tecnologías utilizadas
- Python 3.10+
- openpyxl (lectura/escritura de Excel)
- Simulación en consola (sin API externa)

## Estructura del proyecto
```
mesa-ayuda-bot/
├── bot.py                          # código principal del bot
├── data/
│   └── base_datos_mesa_ayuda.xlsx  # base de datos simulada
└── docs/
    ├── BPMN_AS-IS_MesaAyuda.png    # diagrama del proceso manual
    └── BPMN_TO-BE_MesaAyuda.png    # diagrama del proceso con el bot
```

## Diagramas BPMN del proceso

**AS-IS (proceso manual, sin automatizar):**

<img width="1002" height="722" alt="AS-IS_ Mesa de Ayuda Técnica drawio" src="https://github.com/user-attachments/assets/67b7f0d7-28a3-4fe9-8922-56a86ef8f4a4" />

**TO-BE (proceso automatizado con el chatbot):**

<img width="1302" height="962" alt="Proceso TO-BE_ Chatbot de Mesa de Ayuda Técnica drawio" src="https://github.com/user-attachments/assets/484b2e44-fa37-49e5-8d4d-10832a30b51a" />

## Cómo ejecutarlo
1. Instalar Python 3.10 o superior
2. Instalar la dependencia:
```
pip install openpyxl
```
3. Clonar el repositorio o descargar los archivos
4. Ejecutar desde la terminal, parado en la carpeta del proyecto:
```
python bot.py
```

## Comandos del bot
| Comando | Acción |
|---|---|
| (ninguno) | Al ejecutar `python bot.py`, el bot saluda y pide el legajo directamente |
| `salir` | Cancela la sesión actual |

## Flujo del proceso (resumen)
1. Al iniciar, el bot pide el legajo del usuario (no requiere comandos previos)
2. Usuario indica la categoría del problema (Hardware / Software / Red) y lo describe
3. El bot busca una solución en la base de conocimiento (FAQ)
4. Si encuentra solución - la envía y consulta si se resolvió (Gateway 2)
5. Si no encuentra solución, o el usuario indica que no se resolvió -
   se genera un ticket y se deriva a un técnico de Nivel 2

Si se ingresa un dato inválido en cualquier paso (legajo, categoría,
descripción o confirmación), el bot muestra un mensaje de error y
vuelve a solicitar el mismo dato hasta recibir una respuesta válida.

## Documentación adicional
Los diagramas BPMN (AS-IS y TO-BE), el diccionario de datos, la
máquina de estados y las pruebas de estrés están detallados en el
informe PDF entregado junto con este repositorio.

## Autor
Agustín Ezequiel Fernández — Cohorte Marzo 2026
