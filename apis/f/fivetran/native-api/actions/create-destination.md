# Create Destination with Fivetran

Creates a new destination in your Fivetran account.

## Endpoint

- **Method:** `POST`
- **Path:** `/destinations`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Create Destination](https://fivetran.com/docs/rest-api/api-reference/destination)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `config` | body | `object` | no | Destination setup configuration object. |
| `group_id` | body | `string` | yes | The group ID where the destination belongs. |
| `region` | body | `string` | no | Data processing location. |
| `service` | body | `string` | yes | The destination service type. |
| `time_zone_offset` | body | `string` | yes | The time zone offset used for the Fivetran sync schedule. |
