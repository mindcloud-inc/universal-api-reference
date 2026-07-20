# List Prospect Opportunities with Upnify

Retrieves opportunities for a prospect in Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/prospectos/:tkProspecto/oportunidades`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [List Prospect Opportunities](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-GetProspectosTkprospectoOportunidades)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkProspecto` | path | `string` | yes | El código token que identifica a un prospecto de manera única dentro del CRM, del cual requerimos consultar las oportunidades asociadas.  ¿Dónde obtengo el token? |
