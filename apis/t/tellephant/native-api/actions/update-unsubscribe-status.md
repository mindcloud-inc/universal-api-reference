# Update unsubscribe status with Tellephant

Updates contact subscription status in Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/user/unsubscribe/update`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [Update unsubscribe status](https://app.tellephant.com/api-documentation#update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<string>` | yes | Array of contact phone numbers. |
| `type` | body | `list` | yes | Unsubscribe operation type: unsubscribe, subscribe, block, or unblock. Accepted values: `block`, `subscribe`, `unblock`, `unsubscribe`. |
