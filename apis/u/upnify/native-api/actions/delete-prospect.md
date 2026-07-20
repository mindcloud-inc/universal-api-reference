# Delete Prospect with Upnify

Deletes an existing prospect from Upnify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v4/prospectos/:tkProspecto`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Delete Prospect](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-DeleteProspectosTkprospecto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkProspecto` | path | `string` | yes | El código token que identifica a un prospecto de manera única dentro del CRM, el cual requerimos descartar.  ¿Dónde obtengo el token? |
| `tkRazonPerdida` | query | `string` | yes | Código token que corresponde a una razón de descartado.  ¿Dónde obtengo el token? |
