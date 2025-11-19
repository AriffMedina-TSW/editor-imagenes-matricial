# 📘 Fundamentos de Programación - Práctica 2

## 👨‍💻 Información del Estudiante

- **Nombre:** Ariff Iazid Medina Gómez
- **Matrícula:** SW2509006
- **Grupo:** C
- **Cuatrimestre:** Primer Cuatrimestre
- **Carrera:** TSU en Desarrollo e Innovación de Software
- **Profesor:** Jorge Javier Pedrozo Romero

---

## 📋 Descripción del Proyecto

Este repositorio contiene mi solución a la práctica de **Fundamentos de Programación**, donde programé en JavaScript varias funciones para trabajar con imágenes PNG usando operaciones basadas en álgebra matricial.

## 🎯 Objetivos Alcanzados

- ✅ Dominar variables y tipos de datos en JavaScript
- ✅ Implementar estructuras condicionales
- ✅ Utilizar bucles y funciones
- ✅ Manipular funciones relacionadas a imagenes
- ✅ Trabajar con arrays bidimensionales (matrices)
- ✅ Aplicar control de versiones con Git y GitHub

---

## 📊 Progreso de Ejercicios

### Sección 1: Fundamentos - Conversión Imagen ↔ Matriz (20 puntos)
- [x] 1.1 Cargar imagen pequeña (5 pts) ✅
- [x] 1.2 Guardar matriz como PNG (5 pts) ✅
- [x] 1.3 Extraer canal rojo (5 pts) ✅
- [x] 1.4 Leer dimensiones (5 pts) ✅

**Puntos obtenidos: 20/20**

### Sección 2: Operaciones Básicas (25 puntos)
- [x] 2.1 Aumentar brillo (8 pts) ✅
- [x] 2.2 Negativo de imagen (8 pts) ✅
- [x] 2.3 Blanco y negro (9 pts) ✅

**Puntos obtenidos: 25/25**

### Sección 3: Transformaciones Geométricas (30 puntos)
- [x] 3.1 Efecto espejo (10 pts) ✅
- [x] 3.2 Arriba-abajo (10 pts) ✅
- [x] 3.3 Rotación horaria (10 pts) ✅

**Puntos obtenidos: 30/30**

### Sección 4: Filtros Avanzados (25 puntos)
- [x] 4.1 Blend de dos imágenes (8 pts) ✅
- [x] 4.2 Efecto vintage (9 pts) ✅
- [x] 4.3 Detección simple (8 pts) ✅

**Puntos obtenidos: 25/25**

---

## 📈 Calificación Final

```
┌────────────────────────────────────────┐
│  REPORTE DE CALIFICACIÓN               │
├────────────────────────────────────────┤
│  Puntos obtenidos: 100/100             │
│  Porcentaje: 100%                      │
│  🎓 Calificación: A - Excelente        │
└────────────────────────────────────────┘
```

![Tests](../../actions/workflows/test.yml/badge.svg)

---

## 🚀 Instalación y Uso

### Prerrequisitos
- Node.js (versión 14 o superior)
- Git

### Clonar el repositorio
```bash
git clone https://github.com/TU-USUARIO/fundamentos-programacion-practica-1.git
cd fundamentos-programacion-practica-1
```

### Instalar dependencias
```bash
npm install
```

### Ejecutar tests
```bash
npm test
```

### Ejecutar tests en modo watch
```bash
npm run test:watch
```

### Ver cobertura de código
```bash
npm run test:coverage
```

---

## 📁 Estructura del Proyecto

```
fundamentos-programacion-practica-1/
│
├── ejercicios.js           # ⭐ Archivo principal con mis soluciones
├── ejercicios.test.js      # Tests automatizados (no modificar)
├── package.json            # Configuración del proyecto
├── README.md               # Este archivo
├── GUIA_ESTUDIANTES.md     # Guía de referencia
├── GUIA_INSTRUCTOR.md      # Guía del profesor
│
└── .github/
    └── workflows/
        └── test.yml        # Configuración de GitHub Actions
```

---

## 💡 Aprendizajes Clave

### Lo que más me costó
- **Ejercicio 4.3: Detectar bordes (simplificado)**: Porque combina matrices, recorridos, cálculos matemáticos, comparación de vecinos, control de errores, y conceptos de visión computacional.
- **Ejercicio 3.1 (Factorial)**: Requiere entender cómo se mueven los índices en dos dimensiones al rotar, no solo copiar datos.

### Lo que más me gustó
- **Aplicación práctica de álgebra matricial**: Trabajar con imágenes permitió ver cómo algunas operaciones se aplican directamente sobre datos pixelados.
- **Manipulación directa de píxeles**: Trabajar con valores RGBA a nivel individual te obliga a comprender cómo funciona realmente una imagen a nivel de memoria.

### Técnicas aplicadas
- Manipulación de imágenes en formato `PNG`
- Recorrido sistemático de matrices con `for`
- Uso de `funciones auxiliares` estructuradas
- Bucles anidados para matrices

---

## 🔧 Ejemplos de Código

### Función Favorita: Transponer Matriz
```javascript
function invertirColores(matriz) {
  validarMatriz(matriz);
  const dim = obtenerDimensiones(matriz);
  const nueva = crearMatrizVacia(dim.filas, dim.columnas);

  for (let i = 0; i < dim.filas; i++) {
    for (let j = 0; j < dim.columnas; j++) {
      const p = matriz[i][j];
      nueva[i][j] = crearPixel(
        255 - p.r,
        255 - p.g,
        255 - p.b,
        p.a
      );
    }
  }

  return nueva;
}
```

**Por qué me gusta:** Porque me muestra cómo una operación matemática sencilla puede transformar completamente una imagen (inviertiendo los colores).

---

## 📚 Recursos Utilizados

- [MDN Web Docs - JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript)
- [JavaScript.info](https://es.javascript.info/)
- [Stack Overflow](https://stackoverflow.com)
- Guía del estudiante incluida en el repositorio

---

## 🎯 Próximos Pasos

Este proyecto me prepara para:
- ✨ Entender cómo el álgebra se aplica a imágenes reales 
- 🖼️ Manipular matrices para transformar datos visuales 
- 🔐 Implementar operaciones comunes de edición con lógica matemática  
- 📊 Desarrollar pensamiento lógico aplicando teoría a problemas prácticos

---

## 📝 Historial de Commits

```bash
# Ver mi historial completo
git log --oneline --graph --decorate
```

**Commits destacados:**
- `Pasar imagen a escala de grises en Ejercicio 2.3`
- `Ajustar brillo en Ejercicio 2.1`
- `Conversión de matriz a png en Ejercicio 1.2`
- `Mezclar imagenes en Ejercicio 4.1`
- `Voltear la imagen en horizontal en Ejercicio 3.1`
- `Invertir los colores de la imagen en Ejercicio 2.2`

---

## 🤝 Agradecimientos

- **Profesor Jorge Javier Pedrozo Romero** por la estructura del curso y la práctica
- **Compañeros del Grupo C** por el apoyo mutuo
- **Tecnológico de Software** por la formación integral

---

## 📧 Contacto

- **Email Institucional:** ariff.medina@tecdesoftware.edu.mx
- **GitHub:** @AriffMedina-TSW (https://github.com/AriffMedina-TSW)

---

## 📄 Licencia

Este proyecto es parte de las actividades académicas del **Tecnológico de Software** y está bajo la licencia MIT.

---

<div align="center">

**⭐ Si te gustó este proyecto, dale una estrella ⭐**

Hecho con 💙 por Ariff - 2025

</div>
