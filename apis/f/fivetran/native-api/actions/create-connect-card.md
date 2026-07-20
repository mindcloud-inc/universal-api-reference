# Create Connect Card with Fivetran

Creates a Connect Card for a connection in Fivetran.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections/[:connectionId]/connect-card`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Create Connect Card](https://fivetran.com/docs/rest-api/api-reference/connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connect_card_config` | body | `object` | no | Connect Card configuration object. |
| `connectionId` | path | `string` | yes | The unique identifier for the connection within Fivetran. |
