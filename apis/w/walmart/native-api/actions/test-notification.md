# Test Notification with Walmart

Send a test notification to a destination URL using a sample payload.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/webhooks/test`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Test Notification](https://developer.walmart.com/us-marketplace/reference/getallsubscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventType` | body | `list<string>` | no | Filter results to a specific event type. Refer to the events section for the list of available event types. |
| `resourceName` | body | `list<string>` | no | Filter results to a specific resource (functional category) that the event type maps to. Refer to the events section for the list of available resource names. |
| `eventUrl` | body | `string` | no | Destination URL where notifications are delivered. |
| `eventVersion` | body | `string` | no | — |
