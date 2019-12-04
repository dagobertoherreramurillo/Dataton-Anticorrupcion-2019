# Datatón-Anticorrupción-2019
El "Datatón Anticorrupción" es un hackathon donde construimos herramientas informativas para la sociedad utilizando datos abiertos proporcionados por el Sistema Nacional Anticorrupción (SNA). 

![Aquí la descripción de la imagen por si no carga](imagenes/Modelo_de_grafo_para_contrataciones_públicas.jpg)



LOAD CSV WITH HEADERS FROM 'file:///contracts.csv' AS row
CREATE (contract:Contract{ocid:row.ocid, cycle:row.cycle,
region:row.region, procurementMethod:row.procurementMethod,
amount:row.amount,buyer:row.buyer})
