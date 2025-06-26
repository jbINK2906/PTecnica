# Prueba Técnica – Programador Backend (.NET)

Este proyecto es una **API RESTful de banca** desarrollada con **ASP.NET Core 8, Entity Framework Core y SQLite**, como parte de una prueba técnica para evaluar habilidades en desarrollo backend.

---

## 📌 Funcionalidades implementadas

- ✅ Crear perfil de cliente
- ✅ Crear cuenta bancaria asociada a un cliente
- ✅ Consultar saldo de una cuenta
- ✅ Registrar depósitos y retiros con validación de fondos
- ✅ Ver historial completo de transacciones (incluyendo saldo después de cada una)
- ✅ Inyección de dependencias
- ✅ Pruebas desde Swagger UI y Postman
- ✅ Persistencia con SQLite

---

## 🚀 Tecnologías usadas

- [.NET 8](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- ASP.NET Web API
- Entity Framework Core
- SQLite
- Swagger / OpenAPI
- Visual Studio Code

---

## ⚙️ Requisitos previos

- .NET SDK 8.0
- Visual Studio Code (u otro editor)
- Postman (opcional, para pruebas)
- Git

---

## 🛠️ Instrucciones para ejecutar el proyecto

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git
   cd tu_repositorio
Restaura dependencias y compila el proyecto:

bash
Copy
Edit
dotnet restore
dotnet build
Ejecuta migraciones para crear la base de datos SQLite:

bash
Copy
Edit
dotnet ef migrations add InitialCreate
dotnet ef database update
Ejecuta la API:

bash
Copy
Edit
dotnet run
Accede a Swagger UI en tu navegador:

bash
Copy
Edit
http://localhost:5004/swagger
📬 Endpoints principales
Clientes
Método	URL	Descripción
POST	/api/clientes	Crear cliente
GET	/api/clientes/{id}	Obtener cliente por ID

Cuentas Bancarias
Método	URL	Descripción
POST	/api/cuentas	Crear cuenta
GET	/api/cuentas/{numeroCuenta}/saldo	Consultar saldo actual

Transacciones
Método	URL	Descripción
POST	/api/transacciones/deposito	Registrar depósito
POST	/api/transacciones/retiro	Registrar retiro
GET	/api/transacciones/{numeroCuenta}/historial	Ver historial de transacciones

🧪 Ejemplo de prueba en Swagger
Crear cliente (POST /api/clientes)
json
Copy
Edit
{
  "nombre": "Ana López",
  "fechaNacimiento": "1995-01-01",
  "sexo": "Femenino",
  "ingresos": 8000
}
📝 Notas técnicas
La propiedad numeroCuenta se genera automáticamente con un identificador único.

No se permiten retiros si el saldo disponible es insuficiente.

Las transacciones registran la fecha y el saldo restante.

📂 Base de datos
Se genera automáticamente un archivo banco.db en la raíz del proyecto usando EF Core + SQLite.

📌 Instrucciones finales
Este repositorio está preparado para evaluación técnica.
Para ejecutarlo correctamente, recuerda:

Usar dotnet ef para migraciones

Verificar que Program.cs contenga los servicios y mapeos adecuados

Probar desde Swagger o Postman

👨‍💻 Autor
José Benito Rojas López
Ing. Cibernetica Electronica
Prueba técnica Backend .NET – 2025
