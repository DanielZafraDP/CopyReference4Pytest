# CopyReference4Pytest

[🇪🇸 Español](#-español) | [🇺🇸 English](#-english)

![License](https://img.shields.io/badge/license-MIT--NC-blue)
![JetBrains Plugin](https://img.shields.io/jetbrains/plugin/v/27721)

---

## 🇪🇸 Español

### ¿Qué hace este plugin?

**CopyReference4Pytest** es un plugin para PyCharm que convierte automáticamente las referencias copiadas con "Copy Reference" al formato que necesita pytest para ejecutar tests de Python.

### 🤔 ¿Por qué existe?

Cuando trabajas con Python en PyCharm y usas la función "Copy Reference" (Ctrl+Alt+Shift+C), obtienes rutas como:
```
mi_proyecto.tests.test_usuario.TestUsuario.test_login
mi_proyecto/tests/test_usuario.py
```

Pero pytest necesita el formato con `::` para funciones y clases:
```
mi_proyecto/tests/test_usuario.py::TestUsuario::test_login
```

Este plugin hace la conversión automáticamente, ahorrándote tiempo y errores manuales.

### ✨ Características

- 🔄 **Conversión automática**: Transforma referencias de Java/IntelliJ al formato pytest
- 📋 **Integración con portapapeles**: Usa el sistema de portapapeles de PyCharm (la función "Copy Reference")
- 🎯 **Detección inteligente**: Identifica automáticamente si es una ruta de archivo o referencia de clase/función
- ⚡ **Rápido y simple**: Un solo clic para convertir y copiar
- 🧪 **Compatible con Pytest desde el menú contextual**
- ✅ **Convierte y pega directamente en tu terminal de testeo**

### 🚀 Instalación

#### Desde el repositorio (Desarrollo)
1. Clona este repositorio
2. Abre el proyecto en PyCharm
3. Ejecuta `./gradlew buildPlugin`
4. Ve a `File > Settings > Plugins > ⚙️ > Install Plugin from Disk...`
5. Selecciona el archivo `.zip` generado en `build/distributions/`

### 📖 Uso

1. **Selecciona** cualquier elemento en tu código Python (función, clase, archivo)
2. **Ejecuta** "Copy Reference for Pytest" desde:
   - El menú contextual (clic derecho)
   - Asigna un atajo de teclado personalizado
3. **¡Listo!** La referencia convertida está en tu portapapeles, lista para usar con pytest

### 📝 Ejemplos de conversión

| Entrada (PyCharm Reference)           | Salida (Pytest Format) |
|---------------------------------------|-------------------------|
| `tests.test_auth.TestAuth.test_login` | `tests/test_auth.py::TestAuth::test_login` |
| `src.models.User.validate`            | `src/models.py::User::validate` |
| `tests/test_database.py`              | `tests/test_database.py` |
| `tests/test_database.py:14`           | `tests/test_database.py` |

### 🔧 Desarrollo

#### Requisitos
- PyCharm 2020.3+
- Java 11+
- Gradle

#### Comandos útiles
```bash
# Construir el plugin
./gradlew buildPlugin

# Ejecutar en IDE de desarrollo
./gradlew runIde

# Ejecutar tests
./gradlew test
```

### 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Por favor:
1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -am 'Añadir nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Abre un Pull Request

### 📄 Licencia

Este proyecto está licenciado bajo una variante de la Licencia MIT que **prohíbe usos comerciales**. Consulta el archivo [LICENSE](LICENSE) para más información.

### 🐛 Reportar bugs

¿Encontraste un bug? Por favor abre un [issue](https://github.com/dazdwc/CopyReference4Pytest/issues) con:
- Descripción del problema
- Pasos para reproducir
- Versión de PyCharm
- Ejemplo de input/output esperado

---
### 🌟 Dale una estrella al repositorio si te ha sido útil

Hecho con ❤️ para la comunidad Python

### ❤️ ¿Te ha resultado útil?

Si este plugin te ha ahorrado tiempo o te ha servido de ayuda, puedes invitarme a un café ☕:

☕ [Invítame a un café (PayPal)](https://paypal.me/Shaconeverlose)

---

## 🇺🇸 English

### What does this plugin do?

**CopyReference4Pytest** is a PyCharm plugin that automatically converts references copied with "Copy Reference" to the format pytest needs to run Python tests.

### 🤔 Why does it exist?

When working with Python in PyCharm and using "Copy Reference" (Ctrl+Alt+Shift+C), you get paths like:
```
my_project.tests.test_user.TestUser.test_login
my_project/tests/test_user.py
```

But pytest needs the `::` format for functions and classes:
```
my_project/tests/test_user.py::TestUser::test_login
```

This plugin does the conversion automatically, saving you time and manual errors.

### ✨ Features

- 🔄 **Automatic conversion**: Transforms PyCharm references to pytest format
- 📋 **Clipboard integration**: Uses PyCharm's clipboard system (the "Copy Reference" action)
- 🎯 **Smart detection**: Automatically identifies if it's a file path or class/function reference
- ⚡ **Fast and simple**: One click to convert and copy
- 🧪 **Context menu integration for Pytest**
- ✅ **Convert and paste directly into your test terminal**

### 🚀 Installation

#### From repository (Development)
1. Clone this repository
2. Open the project in PyCharm
3. Run `./gradlew buildPlugin`
4. Go to `File > Settings > Plugins > ⚙️ > Install Plugin from Disk...`
5. Select the generated `.zip` file in `build/distributions/`

### 📖 Usage

1. **Select** any element in your Python code (function, class, file)
2. **Execute** "Copy Reference for Pytest" from:
   - Context menu (right-click)
   - Assign a custom keyboard shortcut
3. **Done!** The converted reference is in your clipboard, ready to use with pytest

### 📝 Conversion examples

| Input (PyCharm Reference) | Output (Pytest Format) |
|----------------------------|-------------------------|
| `tests.test_auth.TestAuth.test_login` | `tests/test_auth.py::TestAuth::test_login` |
| `src.models.User.validate` | `src/models.py::User::validate` |
| `tests/test_database.py` | `tests/test_database.py` |
| `tests/test_database.py:14`           | `tests/test_database.py` |

### 🔧 Development

#### Requirements
- PyCharm 2020.3+
- Java 11+
- Gradle

#### Useful commands
```bash
# Build the plugin
./gradlew buildPlugin

# Run in development IDE
./gradlew runIde

# Run tests
./gradlew test
```

### 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

### 📄 License

This project is licensed under a modified MIT License that **prohibits commercial use**. See the [LICENSE](LICENSE) file for details.

### 🐛 Bug reports

Found a bug? Please open an [issue](https://github.com/dazdwc/CopyReference4Pytest/issues) with:
- Problem description
- Steps to reproduce
- PyCharm version
- Example input/expected output

---

## 🌟 Star this repo if it helps you!

Made with ❤️ for the Python community

## ❤️ Found this useful?

If this plugin saved you time or helped you out, feel free to buy me a coffee ☕:

☕ [buy me a coffee (PayPal)](https://paypal.me/Shaconeverlose)
