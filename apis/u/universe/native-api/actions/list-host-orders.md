# List Host Orders with Universe

Retrieves orders for a specified Universe host.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [List Host Orders](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query document to execute for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables object for the host orders query. |
