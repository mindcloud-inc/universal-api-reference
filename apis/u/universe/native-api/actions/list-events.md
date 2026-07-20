# List Events with Universe

Retrieves events for a specified Universe host.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [List Events](https://developers.universe.com/docs/getting-a-list-of-your-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query or mutation document to execute. The default is an events listing example for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default events query. |
