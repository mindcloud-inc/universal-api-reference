# Get subscriptions with xMatters

Retrieves subscriptions from your xMatters instance.

## Endpoint

- **Method:** `GET`
- **Path:** `subscriptions`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Get subscriptions](https://help.xmatters.com/xmapi/index.html#get-subscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `owner` | query | `string` | no |
| `subscriptionForm` | query | `string` | no |
