# Get Discount with Universe

Retrieves a specific discount from Universe.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [Get Discount](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query or mutation document to execute. The default is a discount detail example for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default discount query. |
