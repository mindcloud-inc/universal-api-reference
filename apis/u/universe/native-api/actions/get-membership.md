# Get Membership with Universe

Retrieves a specific membership from Universe.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [Get Membership](https://developers.universe.com/docs/basic-usage-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query document to execute for this action. |
| `variables` | body | `object` | yes | Optional GraphQL variables object for the membership query. |
