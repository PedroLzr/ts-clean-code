# Guía de Código Limpio en TypeScript

> **Una referencia completa para escribir código limpio y mantenible en TypeScript**

Este documento proporciona una base sólida para escribir código de calidad en TypeScript. Es una referencia que puedes usar en tus proyectos y también está abierta a la colaboración de la comunidad.

## 📏 Longitud de línea

Limita las líneas de código a un máximo de **80 caracteres** para mejorar la legibilidad.

## 🔚 Uso de punto y coma

Siempre utiliza punto y coma (`;`) para finalizar las instrucciones.

```typescript
// Correcto
let x = 1;

// Incorrecto
let x = 1
```

## 💬 Comillas

Usa comillas dobles (`"`) para las cadenas de texto.

```typescript
// Correcto
let foo = "bar";

// Incorrecto
let foo = 'bar';
```

## 🔗 Llaves

Las llaves de apertura deben ir en la misma línea que la declaración.

```typescript
// Correcto
if (true) {
  console.log("ganando");
}

// Incorrecto
if (true)
{
  console.log("perdiendo");
}
```

Apila las cláusulas `else` o `catch` en la misma línea que la llave de cierre:

```typescript
// Correcto
if (i % 2 === 0) {
  console.log("par");
} else {
  console.log("impar");
}
```

## 📌 Declaración de variables

Prefiere `let` en lugar de `var` y usa `const` siempre que sea posible.

```typescript
// Correcto
const button = new Button();

for (let i = 0; i < items.length; i++) {
  // hacer algo
}
```

## 🏷️ Nombres de variables y propiedades

- Usa `camelCase` para variables y propiedades.
- Evita abreviaturas poco comunes.

```typescript
// Correcto
let adminUser = db.query("SELECT * FROM users ...");
```

## 🔠 Nombres de tipos

Utiliza `PascalCase` (camel case en mayúsculas) para nombres de clases y tipos.

```typescript
// Correcto
class UserAccount {
  private field = "a";
}
```

## 🔒 Constantes

Las constantes deben declararse en mayúsculas, separadas por guiones bajos:

```typescript
// Correcto
const TIMEOUT_SECONDS = 60;
```

## 🏗️ Creación de objetos y arrays

- Usa comas finales.
- Mantén las declaraciones cortas en una sola línea.

```typescript
// Correcto
const array = ["hola", "mundo"];
const objeto = {
  clave: "valor",
  otraClave: "otroValor",
};
```

## ⚖️ Operadores de igualdad

Utiliza operadores de comparación estricta (`===` o `!==`).

```typescript
// Correcto
if (a === "") {
  console.log("correcto");
}
```

## 🚩 Uso de llaves en condiciones

Siempre usa llaves, incluso para una sola instrucción:

```typescript
// Correcto
if (a) {
  return "correcto";
}
```

## 🔍 Comparaciones booleanas

Evita comparar directamente con `true` o `false`.

```typescript
// Correcto
if (isValid) {
  console.log("válido");
}
```

## 🔄 Condiciones Yoda

Evita las condiciones Yoda:

```typescript
// Correcto
if (valor >= 0) {
  console.log("correcto");
}
```

## 🧑‍💻 Longitud de funciones

Las funciones deben ser concisas. Trata de que ocupen menos de la mitad de la altura de la pantalla.

## 🔁 Retornos anticipados

Evita la anidación profunda retornando tan pronto como sea posible:

```typescript
// Correcto
function validar(valor: number) {
  if (valor < 0 || valor > 100) {
    return false;
  }
  return true;
}
```

## 🔥 Funciones de flecha

Prefiere las funciones de flecha por su manejo más claro de `this`.

```typescript
// Correcto
req.on("end", () => {
  procesar();
});
```

## 📁 Convención para nombres de archivo

- Usa minúsculas.
- Separa las palabras con guiones (`-`).

```typescript
// Correcto
mi-archivo.ts
```

## 🔐 Variables y métodos privados

Prefija con guion bajo (`_`) los métodos o variables privadas:

```typescript
class Ejemplo {
  private _contador: number;

  private _incrementar() {
    this._contador++;
  }
}
```

## 🔧 Parámetros opcionales en TypeScript

Evita los parámetros opcionales en archivos de implementación:

```typescript
// Correcto
export declare function concatenar(...cadenas: string[]): string;
```

## 🚀 Contribuciones

Este documento está abierto a contribuciones. Si deseas mejorar o sugerir cambios, realiza un *fork* y envía un *pull request*.

---

**¡Mantén tu código limpio y mantenible!** ✨

