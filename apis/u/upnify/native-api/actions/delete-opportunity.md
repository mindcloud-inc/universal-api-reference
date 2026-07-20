# Delete Opportunity with Upnify

Deletes an existing opportunity from Upnify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v4/oportunidades/:tkOportunidad`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Delete Opportunity](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Oportunidades-DeleteOportunidadesTkoportunidad)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkOportunidad` | path | `string` | yes | El código token que identifica a una oportunidad de manera única dentro del CRM, la cual se requiere eliminar.  ¿Dónde obtengo el token? |
