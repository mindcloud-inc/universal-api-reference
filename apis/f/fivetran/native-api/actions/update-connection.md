# Update Connection with Fivetran

Updates an existing connection in your Fivetran account.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/connections/[:connectionId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Update Connection](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth` | body | `object` | no | Connection authorization settings object. |
| `config` | body | `object` | no | Connection setup configuration object. |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
| `paused` | body | `boolean` | no | Whether the connection is paused. |
