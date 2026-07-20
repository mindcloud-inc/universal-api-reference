# Get Host Report with Universe

Retrieves the report preview for a Universe host.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [Get Host Report](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query document to execute for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables object for the host report query. |
