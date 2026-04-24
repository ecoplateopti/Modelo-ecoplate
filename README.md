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

👉 [Descargar dataset completo](data/datos_simulados.xlsx)

## 📊 Dashboard en Power BI

Vista previa del dashboard desarrollado para el análisis de demanda:

![Dashboard Preview](images/dashboard.png)

🔗 **Descargar archivo Power BI (.pbix):**  
[Haz clic aquí para descargar](./dashboard.pbix)

📌 **Aclaración:**  

En esta simulación se asume que el total de platos vendidos es igual al total de clientes.

## 📊 Análisis del dashboard

A partir de la visualización en Power BI, se identifican los siguientes hallazgos clave:

### 💰 Ingresos y volumen de ventas

- **Ingresos totales:** 59,0125 millones  
- **Total de platos vendidos:** 3,462  
- **Total de clientes:** 3,462  

### 📅 Demanda según tipo de día

- **Fin de semana:** ~60% de las ventas  
- **Entre semana:** ~40%  

📌 **Idea:**  
La demanda aumenta significativamente en fines de semana.

👉 **Recomendación:**  
Incrementar producción y abastecimiento en fines de semana, y reducir en días de baja demanda.

### 🧂 Consumo de ingredientes

Ingredientes más utilizados:

- arroz (~3.6 mil)  
- ensalada (~3.6 mil)  
- frijol (~2.0 mil)  
- presa de pollo (~1.8 mil)  

Ingredientes menos utilizados:

- tofu (~0.5 mil)  
- corte de cerdo (~0.4 mil)  

📌 **Idea:**  
Los acompañamientos básicos dominan el consumo, mientras que algunas proteínas tienen menor rotación.

👉 **Recomendación:**  
Optimizar compras enfocándose en ingredientes de alta rotación como carne y pollo y reducir inventario de baja demanda como tofu y cerdo.

### 🍽️ Preferencia de platos

- **Pollo** es el plato más vendido  
- **Carne** tiene demanda intermedia  
- **Cerdo y vegetariano** presentan menor consumo  

📌 **Idea:**  
Existe una preferencia hacia platos con pollo y carne. 

👉 **Recomendación:**  
Ajustar la producción priorizando pollo y carne, y evaluar estrategias para aumentar la demanda de opciones menos consumidas. 

### 🥘 Preferencia de acompañamientos (principio)

- En **pollo**, lenteja supera a frijol  
- En **carne**, frijol domina  
- En **cerdo**, lenteja es más frecuente  

📌 **Idea:**  
Las preferencias de acompañamiento dependen del tipo de plato.

👉 **Recomendación:**  
Preparar combinaciones optimizadas según patrones de consumo para reducir desperdicio.

### 📈 Comportamiento temporal de ventas

- Alta variabilidad diaria  
- Picos de demanda hacia finales de mes  
- Caídas en días específicos entre semana  

📌 **Idea:**  

La demanda no es constante, de manera que resulta util el uso de modelos predictivos. 

## 🧠 Conclusión del análisis

El análisis del dashboard permite evidenciar que el restaurante atendió aproximadamente 3,500 clientes durante el mes de marzo, generando ingresos aproximadamente de 60 millones de pesos, lo que refleja una operación rentable pero con oportunidades de optimización. A partir de los datos, se identifican patrones consistentes en la demanda, especialmente en función del tipo de día, donde los fines de semana presentan una mayor demanda en el consumo en comparación con los días entre semana.

Asimismo, se observa una fuerte preferencia por platos basados en pollo, seguido por la carne. Por otro lado, opciones como cerdo y vegetariano presentan baja rotación, lo que implica un mayor riesgo de desperdicio. Este comportamiento impacta directamente el consumo de ingredientes, donde insumos como arroz, ensalada y frijol muestran alta demanda, mientras que otros asociados a platos menos populares tienen menor uso.

En conjunto, estos hallazgos con las recomendaciones ofrecidas permiten transformar la operación del restaurante hacia un modelo más eficiente, en el que se optimizan recursos, se reduce el desperdicio de alimentos y se maximiza la rentabilidad.

