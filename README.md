📱 Acelerómetro ESP32 con Bluetooth Este proyecto utiliza un ESP32 junto con un sensor MPU6050 para medir aceleración en tres ejes (X, Y, Z) y transmitir los datos en tiempo real vía Bluetooth a través de la app Dabble.

🛠️ Hardware Requerido Placa ESP32 (cualquier versión compatible)

Sensor MPU6050 (acelerómetro y giroscopio)

Cables dupont para conexiones

Fuente de alimentación para el ESP32

🔌 Esquema de Conexiones MPU6050 ESP32 VCC 3.3V GND GND SCL GPIO22 SDA GPIO21 📋 Dependencias del Software Librerías Requeridas: MPU6050 by Electronic Cats

Instalar desde: Gestor de librerías Arduino IDE

Buscar "MPU6050" y instalar

DabbleESP32

Instalar desde: Gestor de librerías Arduino IDE

Buscar "DabbleESP32" y instalar

Entorno de Desarrollo: Arduino IDE 1.8.19 o superior

Board ESP32 en Arduino IDE (instalar desde Board Manager)

⚙️ Configuración y Compilación

Configurar Arduino IDE para ESP32

Abrir Arduino IDE
Ir a Archivo → Preferencias
En "Gestor de URLs adicionales de tarjetas" agregar: https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
Ir a Herramientas → Placa → Gestor de tarjetas
Buscar "ESP32" e instalar
Seleccionar la placa correcta Herramientas → Placa → "ESP32 Dev Module" Herramientas → Puerto → Seleccionar el puerto correcto Herramientas → Flash Frequency → "80MHz" Herramientas → Upload Speed → "115200"

Compilar y Cargar Conectar el ESP32 al ordenador vía USB Verificar que se detecta el puerto COM correcto Hacer clic en "Verificar" para compilar Hacer clic en "Subir" para cargar al ESP32

Configuración de la App Dabble Instalación de la App: Descargar "Dabble" desde: Google Play Store (Android) App Store (iOS)
