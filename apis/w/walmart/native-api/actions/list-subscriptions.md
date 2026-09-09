# List Subscriptions with Walmart

Retrieve details of all webhook subscriptions you've created.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/webhooks/subscriptions`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [List Subscriptions](https://developer.walmart.com/us-marketplace/reference/getallsubscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | Filter results by subscription status. Allowed values: `ACTIVE`, `INACTIVE` |
| `eventType` | query | `list<string>` | no | Filter results to a specific event type. Refer to the events section for the list of available event types. |
| `resourceName` | query | `string` | no | Filter results to a specific resource (functional category) that the event type maps to. Refer to the events section for the list of available resource names. |
| `subscriptionId` | query | `string` | no | Filter results to a specific subscription by its unique identifier. |
