# GraphQL Query with Matterport

Makes an authenticated GraphQL request to Matterport.

## Endpoint

- **Method:** `POST`
- **Path:** `api/models/graph`
- **Base URL:** `https://api.matterport.com/`
- **Official documentation:** [GraphQL Query](https://api.matterport.com/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query to send to Matterport. |
| `variables` | body | `object` | no | GraphQL variables object for the query. |
