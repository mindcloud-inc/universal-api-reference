# List Prospects with Upnify

Retrieves prospects from Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/prospectos`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [List Prospects](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-GetProspectos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aprobacionEstado` | query | `number` | no | Indica el status de asignacion de contacto a compania. - 0 Aprobado. - 1 Pendiente. - 2 Rechazado. |
| `canalizado` | query | `number` | no | Indica si el contacto ha sido canalizado. - 0 No canalizado. - 1 Canalizado. |
| `compartido` | query | `number` | no | Indica si el contacto ha sido compartido. - 0 No compartido. - 1 Compartido. |
| `tkUsuario` | query | `string` | no | Permite filtrar los registros por un usuario en particular. |
| `tkGrupo` | query | `string` | no | Permite filtrar los registros por un grupo en particular. |
| `tkIndustria` | query | `string` | no | Permite filtrar los registros por una industria en particular. |
| `tkEtiqueta` | query | `string` | no | Permite filtrar los registros por una etiqueta en particular. |
| `tkFase` | query | `string` | no | Permite filtrar los registros por una fase en particular. |
| `tkOrigen` | query | `string` | no | Permite filtrar los registros por un origen en particular. |
| `tkCorporativo` | query | `string` | no | Permite filtrar los registros por un corporativo en particular. |
| `idPais` | query | `string` | no | Permite filtrar los registros por un país en particular. |
| `idEstado` | query | `string` | no | Permite filtrar los registros por un estado/región en particular. |
| `sexo` | query | `string` | no | Permite filtrar los registros por un genero en particular. - H Hombre. - M Mujer. |
| `puesto` | query | `string` | no | Permite filtrar los registros por un puesto en particular. |
| `texto` | query | `string` | no | Permite filtrar los registros por un texto en particular. |
| `periodo` | query | `number` | no | Permite filtrar los registros por fecha de creación.  - 1 Hoy. - 2 Ayer. - 3 Esta semana. - 4 Semana anterior. - 5 Este mes. - 6 Mes anterior. - 8 Este año. - 10 Año anterior. - 17 Trimestre actual. - 18 Trimestre anterior. |
| `fechaInicio` | query | `date` | no | Permite filtrar los registros a partir de esta fecha. |
| `fechaFin` | query | `date` | no | Permite filtrar los registros hasta esta fecha. |
| `periodoUltimoContacto` | query | `number` | no | Permite filtrar los registros por fecha de último seguimiento.  - 1 Hoy. - 2 Ayer. - 3 Esta semana. - 4 Semana anterior. - 5 Este mes. - 6 Mes anterior. - 8 Este año. - 10 Año anterior. - 17 Trimestre actual. - 18 Trimestre anterior. |
