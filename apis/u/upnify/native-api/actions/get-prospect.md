# Get Prospect with Upnify

Retrieves a prospect from Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/prospectos/:tkProspecto`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [Get Prospect](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-GetProspectosTkprospecto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tkProspecto` | path | `string` | yes | Código token que identifica a un prospecto de manera única dentro del CRM, del cual se requiere conocer los detalles.  ¿Dónde obtengo el token? |
