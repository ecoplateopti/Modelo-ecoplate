# 🍽️ EcoPlate Optimizer

## 🌱 Descripción
EcoPlate Optimizer es un proyecto de ciencia de datos enfocado en reducir el desperdicio de alimentos en restaurantes mediante modelos predictivos que estiman la demanda diaria.

El sistema permite anticipar cuánta comida preparar, optimizando recursos, reduciendo pérdidas económicas y promoviendo prácticas sostenibles.

## 🚨 Problema

Los restaurantes enfrentan una alta incertidumbre en la demanda:

- Preparar demasiada comida → desperdicio de alimentos  
- Preparar muy poca comida → pérdida de ventas  

En Colombia, los alimentos más desperdiciados incluyen:
- Tomate  
- Papaya  

Esto es especialmente crítico en alimentos perecederos como frutas y vegetales.

## 💡 Solución

EcoPlate Optimizer utiliza datos y modelos predictivos para:

- Predecir el número de clientes diarios  
- Estimar la demanda por tipo de plato  
- Optimizar la producción de alimentos  
- Reducir el desperdicio

## 🧠 Metodología

1. Recolección de datos  
2. Limpieza y análisis exploratorio  
3. Identificación de patrones  
4. Modelado predictivo  
5. Evaluación

## 📁 Datos simulados

El archivo `datos_simulados.xlsx` contiene múltiples hojas que representan el funcionamiento completo de un restaurante.

Estos datos fueron generados de forma simulada y utilizados para el análisis y visualización en Power BI.


## 📊 Estructura del dataset

### 1. 🧾 Ventas marzo

Contiene la demanda diaria de clientes durante el mes de marzo. 

**Variables:**
- `fecha`: día del registro  
- `dia_sem`: día de la semana  
- `tipo_dia`: entre semana o fin de semana  
- `num_clientes`: número de clientes por día  

### 2. 🍽️ Platos vendidos

Describe cuántos platos se vendieron por tipo cada día.

**Variables:**
- `fecha`  
- `total_ventas`: total de clientes ese día  
- `plato`: tipo de plato (pollo, carne, cerdo, vegetariano)  
- `cantidad_vendida`: número de platos vendidos  

### 3. 🥘 Principio del plato

Describe el tipo de acompañamiento escogido por plato.

**Variables:**
- `fecha`  
- `plato`  
- `principio`: (frijol o lenteja)  
- `cantidad`: cantidad consumida  

📌 Se utiliza para analizar patrones de preferencia de acompañamientos.

### 4. 🧂 Ingredientes por plato

Define la composición de cada plato.

**Variables:**
- `plato`  
- `ingrediente`  
- `tipo_ingrediente`: proteína, acompañamiento o principio  

📌 Permite modelar el consumo de insumos.

### 5. 💰 Precios

Contiene el precio de cada tipo de plato.

**Variables:**
- `plato`  
- `precio`  

📌 Permite calcular ingresos y rentabilidad.

### 6. 🏷️ Categorías de platos

Clasificación de los platos según su tipo.

**Ejemplo:**
- pollo → proteína  
- carne → proteína  
- cerdo → proteína  
- vegetariano → saludable  

📌 Permite segmentar análisis por tipo de producto.

## 🧠 Descripción general

El dataset simula un sistema real de un resturante tipo "corriente "donde:

- La demanda varía según el día de la semana  
- Los fines de semana presentan mayor número de clientes  
- Los clientes eligen entre diferentes tipos de platos  
- Cada plato tiene una composición de ingredientes específica  
- Se pueden estimar ingresos y consumo de insumos  

Este enfoque permite realizar análisis de:
- reducción de desperdicio (objetivo principal)
- predicción de demanda  
- optimización de producción  

## 🔗 Relación entre tablas

Las hojas están conectadas mediante:

- `fecha` → conecta ventas y platos vendidos  
- `plato` → conecta platos, ingredientes, precios y categorías  

Esto permite construir un modelo relacional en Power BI.

## 📥 Archivo

👉 [Descargar dataset completo](data/demanda_simulada.xlsx)

## 📊 Dashboard en Power BI

Vista previa del dashboard desarrollado para el análisis de demanda:

![Dashboard Preview](images/dashboard.png)

🔗 **Descargar archivo Power BI (.pbix):**  
[Haz clic aquí para descargar](./dashboard.pbix)


