# List Sales with Upnify

Retrieves sales from Upnify.

## Endpoint

- **Method:** `GET`
- **Path:** `v4/ventas`
- **Base URL:** `https://api.upnify.com`
- **Official documentation:** [List Sales](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-GetVentas)

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
| `periodo` | query | `string` | no | Permite filtrar los registros por fecha de creación. |
| `periodoUltimoContacto` | query | `string` | no | Permite filtrar los registros por fecha de último seguimiento. |
| `tkMoneda` | query | `string` | no | Permite filtrar los registros por una moneda en particular. |
| `tkLinea` | query | `string` | no | Permite filtrar los registros por una linea en particular. |
| `camposAdicionales` | query | `number` | no | Envíe un 1 si dedea que la respuesta devuelva campos personalizados de Prospectos y Oportunidades. |
