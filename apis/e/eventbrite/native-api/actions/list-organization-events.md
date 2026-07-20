# List Organization Events with Eventbrite

Retrieves organization events from Eventbrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/events/`
- **Base URL:** `https://www.eventbriteapi.com/v3`
- **Official documentation:** [List Organization Events](https://www.eventbrite.com/platform/api#/reference/event/list/list-events-by-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | Eventbrite organization identifier (for example, 123456789012). |
