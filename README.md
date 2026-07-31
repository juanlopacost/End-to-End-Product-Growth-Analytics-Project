# Evaluando el impacto de RappiPlus con datos

## Desafío
RappiPlus se diseñó como un servicio de suscripción para aumentar la frecuencia de compra y el valor generado por cada usuario dentro del ecosistema de Rappi. Sin embargo, el equipo de negocio no tenía certeza de si la membresía realmente estaba cumpliendo su objetivo. 

Las dudas clave a resolver eran:
* **Confiabilidad:** ¿Podemos confiar en la calidad de los datos de pedidos, catálogo y marketing?
* **Rentabilidad:** ¿El servicio genera ingresos netos positivos o incurre en pérdidas?
* **Pérdida de usuarios:** ¿En qué etapa del proceso de compra abandonan los usuarios?
* **Retención:** ¿Los suscriptores realmente regresan y compran con mayor frecuencia?
* **Impacto:** ¿Los cambios e hipótesis probados generan un impacto positivo medible?

---
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-003B57?style=for-the-badge&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

## Datos Utilizados
- **rappiplus_orders_raw.csv** → información de pedidos, precios, descuentos y revenue  
- **rappiplus_catalog.csv** → costos de productos, categorías y proveedores  
- **rappiplus_marketing_spend.csv** → inversión en marketing por canal y país  
- **events / users / user_activity (SQL)** → comportamiento del usuario dentro de la plataforma  
- **experiment_checkout_ui.csv** → resultados de un experimento A/B en el checkout  

---
## Proceso
Para responder a estas preguntas, construí un pipeline de analítica end-to-end integrando **Python**, **SQL** y **Power BI/Tableau**, siguiendo una metodología de 6 pasos:

1. **Calidad de Datos (Python):** Limpieza, manejo de nulos y validación de consistencia en los datasets de pedidos, catálogo y marketing.
2. **Análisis de Rentabilidad (Python):** Modelado de ingresos vs. costos operativos para entender el margen real generado por usuario.
3. **Funnel de Conversión (SQL):** Mapeo y consulta del embudo de compra para detectar los puntos exactos de fuga (*drop-offs*).
4. **Análisis de Retención y Cohortes (SQL):** Medición de la recurrencia de los usuarios y comparación del comportamiento entre miembros RappiPlus vs. usuarios regulares.
5. **Experimentación y Pruebas de Hipótesis (Python):** Evaluación del impacto estadístico de cambios en el servicio para validar si realmente incrementan el consumo.
6. **Visualización y Storytelling (Power BI / Tableau):** Creación de un dashboard ejecutivo e interactivo para comunicar hallazgos y recomendaciones estratégicas a los stakeholders.

---

## Resultado y Lecciones
* **Claridad en la rentabilidad:** Se definió con precisión el valor neto por usuario, identificando qué segmentos de clientes hacen que el modelo de suscripción sea sostenible.
* **Optimización del embudo:** Se identificaron las fases críticas del checkout donde se perdía la mayor cantidad de conversiones, permitiendo enfocar esfuerzos de producto en esos fricciones.
* **Confirmación de la recurrencia:** Se demostró mediante análisis de cohortes el patrón de retención real de los usuarios RappiPlus frente a los no suscriptores.
* **Toma de decisiones basada en evidencia:** El dashboard centralizado permitió al equipo de negocio pasar de suposiciones a decisiones estratégicas respaldadas por datos e hipótesis validadas.

<img width="1622" height="685" alt="image" src="https://github.com/user-attachments/assets/c3e2f80d-f581-436f-8ada-b96189d58a90" />
<img width="1506" height="705" alt="image" src="https://github.com/user-attachments/assets/67fb84d8-2d3e-4673-8082-cab79281746d" />
