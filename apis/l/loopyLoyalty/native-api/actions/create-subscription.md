# Create Subscription with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Create Subscription](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createSubscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Target URL to POST the event data to. |
| `event` | body | `string` | yes | Event type that triggers the POST. |
| `cardId` | body | `string` | yes | Campaign ID. |
