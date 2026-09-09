# Create Subscription with Walmart

Create one or more webhook subscriptions for event notifications by selecting an event type, event version, resource name, and providing a destination event URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/webhooks/subscriptions`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Create Subscription](https://developer.walmart.com/us-marketplace/reference/getallsubscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[].status` | body | `list<string>` | no | Filter results by subscription status. Allowed values: `ACTIVE`, `INACTIVE` |
| `events[].eventType` | body | `list<string>` | no | Filter results to a specific event type. Refer to the events section for the list of available event types. |
| `events[].resourceName` | body | `list<string>` | no | Filter results to a specific resource (functional category) that the event type maps to. Refer to the events section for the list of available resource names. |
| `events[].eventVersion` | body | `string` | no | — |
| `events[]` | body | `array<object>` | no | — |
| `events[].eventUrl` | body | `string` | no | Destination URL where notifications are delivered. |
