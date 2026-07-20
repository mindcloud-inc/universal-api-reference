# Check In Order Item with Universe

Checks in a specific Universe order item.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [Check In Order Item](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query or mutation document to execute. The default is an order-item check-in mutation for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default check-in mutation. |
