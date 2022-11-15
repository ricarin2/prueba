![AtresMedia](https://www.atresmediacorporacion.com/public/img/rc-television.svg)
## Tabla de Contenidos ETL
1. [Change Log](#change-log)
2. [Descripción del Proyecto](#descripción-del-proyecto)
3. [Configuración DynamoDB](#configuración-dynamodb)
4. [NoteBooks](#notebooks)

## Change Log
| Versión | Fecha | Descripción |
| --- | --- |--- |
| 1.1.0.0 | xx/11/2022 | Campaign atresplayer_formato (agregada) e incremental |
| 1.0.0.0 | 18/10/2022 | Campaign atresplayer_video (desagregada) e incremental |

## Descripción del Proyecto
Genera los ficheros necesarios para campañas de
- Video (desagregada)
- Formato (agregada)

| Command | Description |
| --- | --- |
| Nombre del Proyecto | atresmedia.campaign.atresplayer.video |
| Proyecto Jenkins | http://internal-jenki-maste-15ns6hhzjhwv6-642896963.eu-west-1.elb.amazonaws.com/job/atresmedia.transformation.campaign.atresplayer.video/|
| Documento operaciones | [ATR - IT - PROC - Campaing_Atresplayer_Video_DS_ETL_Daily_v1.2.0](https://atresmedia.sharepoint.com/:w:/s/PROYECTOBIGDATA-I3TELEVISION/EQJRbxTmm3hCoOsBBXm2JGIBj6sHpGxR1dK0IV5Lwv4QKg)|

## Configuración DynamoDB
**Toda la configuración de DynamoDB del proyecto se puede consultar en el directorio src/resources/dynamoDB**

## NoteBooks
logic implementation and test:
*/src/resources/notebook*
