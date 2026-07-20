# Create Client with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Create Client](https://docs.leantime.io/api/classes/Leantime/Domain/Clients/Services/Clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.values.name` | body | `string` | yes | Client name. |
| `params.values.street` | body | `string` | no | Street address. |
| `params.values.zip` | body | `string` | no | Postal code. |
| `params.values.city` | body | `string` | no | City. |
| `params.values.state` | body | `string` | no | State or region. |
| `params.values.country` | body | `string` | no | Country. |
| `params.values.phone` | body | `string` | no | Phone number. |
| `params.values.internet` | body | `string` | no | Website URL. |
| `params.values.email` | body | `string` | no | Email address. |
