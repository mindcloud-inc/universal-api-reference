# Get Order Item with Universe

Retrieves a specific order item from Universe.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [Get Order Item](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query or mutation document to execute. The default is an order item detail example for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default order item query. |
