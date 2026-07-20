# List Host Events With Tickets with Universe

Retrieves ticketed events for a specified Universe host.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [List Host Events With Tickets](https://developers.universe.com/docs/getting-a-list-of-your-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query document to execute for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables object for the host events query. |
