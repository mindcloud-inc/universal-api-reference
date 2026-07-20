# List Event Access Keys with Universe

Retrieves access keys for a specific Universe event.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [List Event Access Keys](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query or mutation document to execute. The default is an event access-key example for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default access-key query. |
