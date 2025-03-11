# Guía de Código Limpio en TypeScript

Este documento establece una base para escribir código de calidad en TypeScript. Sirve como una referencia que puedes aplicar en tus proyectos para garantizar un código limpio, legible y consistente entre todos los desarrolladores. Al promover buenas prácticas y uniformidad en el formato del código, busca facilitar la colaboración y mejorar el mantenimiento a largo plazo. Este documento está abierto a la contribución de la comunidad.

## 🏷️ Convenciones de Nomenclatura

### 🔡 Variables y Propiedades
- Usa `lowerCamelCase` para variables y propiedades.

### 🏛️ Tipos, Interfaces y Clases
- Emplea `PascalCase` para clases, interfaces y tipos.

### 🚩 Enums
- Nombres de enums en `PascalCase` y sus valores en `UPPER_SNAKE_CASE`.

### 📁 Archivos
- Nombres de archivo en `lowercase-kebab-case`.

### 🔒 Modificadores de Acceso
- Usa `private`, `protected` y `public` para la visibilidad de los miembros de clase.

## Reglas de Formato

### 📏 Longitud de línea

Limita las líneas de código a un máximo de **80 caracteres** para mejorar la legibilidad.

### 🔚 Uso de punto y coma

Siempre utiliza punto y coma (`;`) para finalizar las instrucciones.

```typescript
// Correcto
let x = 1;

// Incorrecto
let x = 1
```

### 💬 Comillas

Usa comillas dobles (`"`) para las cadenas de texto.

```typescript
// Correcto
let foo = "bar";

// Incorrecto
let foo = 'bar';
```

### 🔗 Llaves

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

### 📌 Declaración de variables

Prefiere `let` en lugar de `var` y usa `const` siempre que sea posible.

```typescript
// Correcto
const button = new Button();

for (let i = 0; i < items.length; i++) {
  // hacer algo
}
```

### 🏗️ Creación de objetos y arrays

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

### ⚖️ Operadores de igualdad

Utiliza operadores de comparación estricta (`===` o `!==`).

```typescript
// Correcto
if (a === "") {
  console.log("correcto");
}
```

### 🚩 Uso de llaves en condiciones

Siempre usa llaves, incluso para una sola instrucción:

```typescript
// Correcto
if (a) {
  return "correcto";
}
```

### 🔍 Comparaciones booleanas

Evita comparar directamente con `true` o `false`.

```typescript
// Correcto
if (isValid) {
  console.log("válido");
}
```

### 🔄 Condiciones Yoda

Evita las condiciones Yoda:

```typescript
// Correcto
if (valor >= 0) {
  console.log("correcto");
}
```

### 🧑‍💻 Longitud de funciones

Las funciones deben ser concisas. Trata de que ocupen menos de la mitad de la altura de la pantalla.

### 🔁 Retornos anticipados

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

### 🔥 Funciones de flecha

Prefiere las funciones de flecha por su manejo más claro de `this`.

```typescript
// Correcto
req.on("end", () => {
  procesar();
});
```

### 📁 Convención para nombres de archivo

- Usa minúsculas.
- Separa las palabras con guiones (`-`).

```typescript
// Correcto
mi-archivo.ts
```

### 🔐 Variables y métodos privados

Prefija con guion bajo (`_`) los métodos o variables privadas:

```typescript
class Ejemplo {
  private _contador: number;

  private _incrementar() {
    this._contador++;
  }
}
```

### 🔧 Parámetros opcionales en TypeScript

Evita los parámetros opcionales en archivos de implementación:

```typescript
// Correcto
export declare function concatenar(...cadenas: string[]): string;
```

---

## 💡 Mejores Prácticas

- ✅ Evita comentarios innecesarios: El código debe ser **autoexplicativo**.
- ✅ Tipa explícitamente variables y funciones en TypeScript.
- ✅ Usa funciones puras siempre que sea posible.
- ✅ Evita abreviaciones innecesarias para mejorar la legibilidad.
- ✅ Documenta con JSDoc las funciones y clases públicas:

```typescript
/**
 * Calcula la suma de dos números.
 * @param a Primer número
 * @param b Segundo número
 * @returns Suma de a y b
 */
function sum(a: number, b: number): number {
  return a + b;
}
```

---

## 🤝 Cómo Contribuir

¡Las contribuciones son bienvenidas! 🙌

1. Haz un **fork** de este repositorio.
2. Crea una nueva rama con tu propuesta:
   ```
   git checkout -b feature/tu-mejora
   ```
3. Realiza tus cambios siguiendo las convenciones establecidas.
4. Haz un **commit** con un mensaje claro:
   ```
   git commit -m "Añade nueva práctica de código limpio"
   ```
5. Envía un **pull request** explicando tu cambio.

### 📋 Reglas para Contribuciones
- Sigue las reglas de formato y estilo de este documento.
- Asegúrate de que tu código pase las validaciones de ESLint y Prettier.
- Aporta ejemplos claros y concisos.

---

## 📜 Licencia

Este proyecto está bajo la [Licencia MIT](LICENSE).

---

## 🚀 Créditos

Esta guía ha sido desarrollada para la comunidad y está abierta a futuras mejoras. Siéntete libre de proponer cambios, abrir issues o simplemente dar ⭐️ al proyecto si te resulta útil.

---
