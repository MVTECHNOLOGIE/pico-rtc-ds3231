Librería de MicroPython para Raspberry Pi Pico y RTC DS3231
Este proyecto es una librería profesional y fácil de usar, diseñada para la comunicación entre una Raspberry Pi Pico y el módulo de Reloj de Tiempo Real (RTC) DS3231. Está optimizada para que estudiantes y aficionados puedan implementar funciones de tiempo y temperatura en sus proyectos de manera sencilla y eficiente.

Características
Configuración Automática: Sincroniza la hora del RTC con la hora de tu PC.

Configuración Manual: Permite establecer una hora y fecha específicas de forma manual.

Lectura Modular: Ofrece funciones separadas para leer la hora, la fecha y la temperatura.

Control de Formato: Permite cambiar fácilmente entre el formato de 12 y 24 horas.

Manejo de Errores: Incluye mensajes claros si el módulo no se detecta.

Requisitos
Hardware:

Placa Raspberry Pi Pico (o similar con MicroPython).

Módulo de Reloj de Tiempo Real (RTC) DS3231.

Cables de conexión.

Software:

MicroPython instalado en la Raspberry Pi Pico.

IDE Thonny (recomendado para la programación).

Instalación y Uso
Conecta el Hardware:
Conecta el módulo DS3231 a tu Raspberry Pi Pico utilizando la interfaz I2C. Los pines recomendados son:

VCC -> 3V3

GND -> GND

SDA -> GP0

SCL -> GP1

Sube los Archivos:
Carga los siguientes archivos a tu Raspberry Pi Pico usando Thonny:

ds3231.py (la librería principal)

configurar_automatico.py

configurar_manual.py

Visor.py

Sincronización Inicial (Recomendado):
Abre el archivo configurar_automatico.py y ejecútalo. Esto sincronizará el reloj con la hora de tu PC. Después de la primera ejecución, comenta la línea reloj.sync_from_pc() para que el reloj use su propia batería y no se reinicie.

Usa los Ejemplos:

configurar_automatico.py: Sincroniza la hora con el PC de forma automática.

configurar_manual.py: Muestra cómo establecer la hora manualmente.

Visor.py: Ejecuta un visor que se actualiza cada segundo, mostrando la hora, fecha y temperatura.

Estructura del Proyecto
.
├── ds3231.py                  # La librería principal
├── configurar_automatico.py   # Script para sincronizar con el PC
├── configurar_manual.py       # Script para configurar la hora manualmente
├── Visor.py                   # Script para un visor que muestra los datos en tiempo real
└── README.md                  # Este archivo
Contribuciones
Si tienes ideas para mejorar la librería, ¡siéntete libre de contribuir!

Licencia
Este proyecto está bajo la Licencia MIT.
