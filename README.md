# Análisis de Redes Cliente-Servicio: COVID vs Post-COVID

## Colaboradores
- Francesca Nicole Bances Torres
- Marcelo Matias Hernandez Rengifo 
- Piero Aldair Rivas Pinto

## Resumen
Se analiza la transformación estructural de una red cliente-servicio comparando dos periodos: **COVID (2020–2021)** y **Post-COVID (2022–2023)**. Se construyeron redes cliente-cliente a partir de proyecciones de la red bipartita original, revelando cambios significativos en escala, conectividad, modalidades de servicio y cohesión de la red.

## Objetivos
- Comparar la estructura de la red cliente-servicio durante y post-pandemia.  
- Identificar clientes clave y hubs de conexión.  
- Evaluar cohesión, conectividad y comunidades de la red.  
- Analizar la evolución de modalidades y diversidad de servicios.  

## Metodología

### Datos
- **Dataset:** 10,384 registros de interacciones cliente-servicio (2019–2024)  
- **Variables principales:** Año, Cliente, Tipo de Servicio, Tarea, Modalidad (Presencial/Virtual), Complejidad (Baja/Media/Alta)  

### Preprocesamiento
- Homogeneización de nombres de columnas  
- Eliminación de duplicados  
- Verificación de valores nulos  
- Estadísticas básicas y visualización exploratoria (EDA)  

### Construcción de la Red
- Red bipartita Cliente–Servicio proyectada a Cliente–Cliente  
- Enlaces entre clientes definidos por servicios compartidos  
- Análisis por periodos: COVID (2020–2021) y Post-COVID (2022–2023)  

### Análisis
- Métricas globales: nodos/aristas, densidad, diámetro, APL, clustering, asortatividad  
- Métricas de grado y strength promedio  
- Centralidades: degree, betweenness, closeness  
- Detección de comunidades con algoritmo Louvain  

### Herramientas
- **Lenguaje:** Python  
- **Entorno:** Google Colab  
- **Librerías:** Pandas, NumPy, NetworkX, community_louvain, Matplotlib, Seaborn, Collections  

## Resultados

| Periodo           | Diámetro | APL  | Clustering Global | Clustering Promedio | Modularidad |
|------------------|----------|------|-----------------|-------------------|-------------|
| COVID 20-21       | 2        | 1.422| 0.908           | 0.962             | 0.314       |
| Post-COVID 22-23  | 4        | 2.400| 0.871           | 0.422             | 0.317       |

- **COVID:** Red compacta y concentrada, hubs muy conectados, servicios dominantes SERV_1 y SERV_2.  
- **Post-COVID:** Red más dispersa, hubs menos extremos, mayor diversidad de servicios.  
- **Cohesión comunitaria:** Estable, modularidad simi
