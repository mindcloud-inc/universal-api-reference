# Create Connection with Fivetran

Creates a new connection in your Fivetran account.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Create Connection](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth` | body | `object` | no | Connection authorization settings object when the connector supports API-based authorization. |
| `config` | body | `object` | no | Connection setup configuration object. |
| `group_id` | body | `string` | yes | The group ID where the connection belongs. |
| `paused` | body | `boolean` | no | Whether the connection is paused. |
| `service` | body | `string` | yes | The connector service type. |
| `sync_frequency` | body | `number` | no | The connection sync frequency in minutes. |
