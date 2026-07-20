# List Memberships with Universe

Retrieves memberships for the authenticated viewer in Universe.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [List Memberships](https://developers.universe.com/docs/basic-usage-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query or mutation document to execute. The default is a membership-focused example for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default memberships query. |
