# Retrieve scheduled SMS request with Webex Interact

Finds a scheduled SMS request in Webex Interact by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/v1/scheduled`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Retrieve scheduled SMS request](https://docs.webexinteract.com/reference/scheduled-messages-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter.id` | body | `string` | yes | Scheduled SMS request ID to retrieve. |
