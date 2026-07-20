# List Event Attendees with Universe

Retrieves attendees for a specific Universe event.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://www.universe.com`
- **Official documentation:** [List Event Attendees](https://developers.universe.com/docs/what-data-is-available)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Universe GraphQL query or mutation document to execute. The default is an event attendees example for this action. |
| `variables` | body | `object` | no | Optional GraphQL variables as a JSON object string for the default attendees query. |
