![AtresMedia](https://www.atresmediacorporacion.com/public/img/rc-television.svg) 

## Tabla de Contenidos ETL 
1. [Change Log](change-log)
2. [Descripción del Proyecto](#descripción-del-proyecto)
3. [Parámetros Input Output](parámetros-input-output)
4. [CloudFormation](#cloudformation)
5. [Documentación](#documentación)
6. [NoteBooks](#notebooks)

## Change Log

| Fecha | Descripción | Versión |
| --- | --- |--- |
| 1.1.0.0 | xx/11/2022 | Campaign atresplayer_formato (agregada) e incremental |
| 1.0.0.0 | 18/10/2022 | Campaign atresplayer_video (desagregada) e incremental |

## Descripción del Proyecto

Genera los ficheros necesarios para campañas de
- Video (desagregada)
- Formato (agregada)

| Command | Description |
| --- | --- |
| Nombre del Proyecto | xxx |
| Proyecto Jenkins | Name of Project |
| Dependencias | Write down which are the dependencies |
| Step implicados | (Normalization, Transformation, Transformation CSV) |
| Exports | () |

## Parámetros Input Output

### Argumentos de entrada:
- --**source_name** (required):
- --**start_date** (optional): yyyy-mm-dd
- --**end_date** (optional): yyyy-mm-dd
***
### Ficheros que genera
bucket: datalake.atresmedia.bigdata.pro

- transformed/campaign/campaign_atresplayer_video
- transformed/campaign/campaign_atresplayer_video_inc
- transformed/campaign/campaign_atresplayer_formato
- transformed/campaign/campaign_atresplayer_formato_inc
***
### Configuración en DynamoDB:
The S3 paths for normalized/tranformed are defined on DynamoDB table *atresmedia.sources.catalog* with keys:
- *campaign_atresplayer_video*
- *campaign_atresplayer_video_inc*
- *campaign_atresplayer_formato*
- *campaign_atresplayer_formato_inc*
**Toda la configuración de DynamoDB del proyecto se puede consultar en el directorio src/resources/dynamoDB**

## CloudFormation
Genera los siguientes recursos:
 - **Step Machine**: a3m${Environment}-stepfunction-sm-campaign-atresplayer-video
 - **Rule** (Para video): a3m${Environment}-stepfunction-sm-campaign-atresplayer-video-rule
 - **Rule** (para Formato): a3m${Environment}-stepfunction-sm-campaign-atresplayer-formato-rule

## Documentación
### Documentos de operaciones:
- [ATR - IT - PROC - Campaing_Atresplayer_Video_DS_ETL_Daily_v1.2.0](https://atresmedia.sharepoint.com/:w:/s/PROYECTOBIGDATA-I3TELEVISION/EQJRbxTmm3hCoOsBBXm2JGIBj6sHpGxR1dK0IV5Lwv4QKg)

## NoteBooks
¿Como se ejecuta el código? 
logic implementation and test: 
 */src/resources/notebook*
