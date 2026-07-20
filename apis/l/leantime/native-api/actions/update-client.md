# Update Client with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Update Client](https://docs.leantime.io/api/classes/Leantime/Domain/Clients/Services/Clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | body | `number` | yes | The Leantime client id to update. |
| `params.params.name` | body | `string` | no | Updated client name. |
| `params.params.street` | body | `string` | no | Street address. |
| `params.params.zip` | body | `string` | no | Postal code. |
| `params.params.city` | body | `string` | no | City. |
| `params.params.state` | body | `string` | no | State or region. |
| `params.params.country` | body | `string` | no | Country. |
| `params.params.phone` | body | `string` | no | Phone number. |
| `params.params.internet` | body | `string` | no | Website URL. |
| `params.params.email` | body | `string` | no | Email address. |
