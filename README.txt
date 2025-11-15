📱 Acelerómetro ESP32 con Bluetooth
Este proyecto utiliza un ESP32 junto con un sensor MPU6050 para medir aceleración en tres ejes (X, Y, Z) y transmitir los datos en tiempo real vía Bluetooth a través de la app Dabble.

🛠️ Hardware Requerido
Placa ESP32 (cualquier versión compatible)

Sensor MPU6050 (acelerómetro y giroscopio)

Cables dupont para conexiones

Fuente de alimentación para el ESP32

🔌 Esquema de Conexiones
MPU6050	ESP32
VCC	3.3V
GND	GND
SCL	GPIO22
SDA	GPIO21
📋 Dependencias del Software
Librerías Requeridas:
MPU6050 by Electronic Cats

Instalar desde: Gestor de librerías Arduino IDE

Buscar "MPU6050" y instalar

DabbleESP32

Instalar desde: Gestor de librerías Arduino IDE

Buscar "DabbleESP32" y instalar

Entorno de Desarrollo:
Arduino IDE 1.8.19 o superior

Board ESP32 en Arduino IDE (instalar desde Board Manager)

⚙️ Configuración y Compilación
1. Configurar Arduino IDE para ESP32
cpp
1. Abrir Arduino IDE
2. Ir a Archivo → Preferencias
3. En "Gestor de URLs adicionales de tarjetas" agregar:
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
4. Ir a Herramientas → Placa → Gestor de tarjetas
5. Buscar "ESP32" e instalar
2. Seleccionar la placa correcta
cpp
Herramientas → Placa → "ESP32 Dev Module"
Herramientas → Puerto → Seleccionar el puerto correcto
Herramientas → Flash Frequency → "80MHz"
Herramientas → Upload Speed → "115200"
3. Compilar y Cargar
cpp
1. Conectar el ESP32 al ordenador vía USB
2. Verificar que se detecta el puerto COM correcto
3. Hacer clic en "Verificar" para compilar
4. Hacer clic en "Subir" para cargar al ESP32
📱 Configuración de la App Dabble
Instalación de la App:
Descargar "Dabble" desde:

Google Play Store (Android)

App Store (iOS)

Conexión Bluetooth:
cpp
1. Abrir la app Dabble
2. Ir a "Settings" → "Bluetooth Settings"
3. Buscar y seleccionar "ESP32_Acelerometro"
4. Conectar al dispositivo
5. Volver al menú principal y seleccionar "Terminal"
🚀 Ejecución del Programa
Secuencia de Inicialización:
Alimentar el ESP32

Abrir Monitor Serial (115200 baudios) para verificar:

✅ "Bluetooth iniciado. Conéctate desde la app Dabble."

✅ "Iniciando sensor MPU6050..."

✅ "MPU6050 conectado correctamente"

Conectar desde la app Dabble al dispositivo Bluetooth

Salida de Datos:
Monitor Serial: Valores de aceleración en g (gravedad terrestre)

Terminal Dabble: Datos en tiempo real formateados

📊 Interpretación de Datos
Los valores de aceleración se muestran en unidades de g (9.8 m/s²):

Valor típico en reposo: Z ≈ 1g, X ≈ 0g, Y ≈ 0g

Rango típico: ±2g (configuración por defecto MPU6050)

🐛 Solución de Problemas
Error común: "No se detecta el MPU6050"
cpp
❌ Posibles causas:
   - Conexiones SDA/SCL incorrectas
   - Alimentación insuficiente (usar 3.3V)
   - Sensor MPU6050 defectuoso
Error común: Bluetooth no conecta
cpp
❌ Soluciones:
   - Reiniciar el ESP32
   - Verificar que el nombre en la app coincida
   - Reiniciar Bluetooth del móvil
📁 Estructura del Proyecto
text
ESP32_Acelerometro/
├── src/
│   └── ESP32_Acelerometro.ino
├── docs/
│   └── esquema_conexiones.png
├── README.md
└── library.json
🔄 Historial de Commits
text
commit 1: Implementación inicial - Lectura básica del MPU6050
commit 2: Integración Bluetooth con Dabble - Transmisión en tiempo real
👨‍💻 Autor
Proyecto desarrollado para demostración de capacidades de ESP32 con sensores IMU y comunicación Bluetooth.

⚠️ Nota: Asegúrese de tener las librerías actualizadas para evitar conflictos de compatibilidad.