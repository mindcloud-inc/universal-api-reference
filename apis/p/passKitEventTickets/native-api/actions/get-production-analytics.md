# Get Production Analytics with PassKit Event Tickets

Retrieves production analytics from PassKit.

## Endpoint

- **Method:** `GET`
- **Path:** `/eventTickets/production/:classId/analytics`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Production Analytics](https://docs.passkit.io/protocols/event-tickets/#operation/EventTickets_getAnalytics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `classId` | path | `string` | yes | PassKit production class id for analytics. |
| `protocol` | query | `string` | yes | Analytics protocol to report on. |
