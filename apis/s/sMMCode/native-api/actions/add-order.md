# Add Order with SMMCode

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2`
- **Base URL:** `https://extended.smmcode.org`
- **Official documentation:** [Add Order](https://extended.smmcode.org/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | body | `string` | yes | Service ID from the SMMCode service list. |
| `link` | body | `string` | yes | Link to the page for the order. |
| `quantity` | body | `number` | yes | Needed quantity for the order. |
| `runs` | body | `number` | no | Optional runs to deliver when supported by the selected service. |
| `interval` | body | `number` | no | Optional interval in minutes when supported by the selected service. |
