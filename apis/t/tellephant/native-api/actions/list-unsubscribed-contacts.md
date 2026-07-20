# List unsubscribed contacts with Tellephant

Retrieves contacts by subscription status from Tellephant.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/user/unsubscribe`
- **Base URL:** `https://api.tellephant.com`
- **Official documentation:** [List unsubscribed contacts](https://app.tellephant.com/api-documentation#get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `list` | yes | Contact list type: all, unsubscribed, or blocked. Accepted values: `all`, `blocked`, `unsubscribed`. |
