# Create Feedback with Product Fruits

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/feedback`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Create Feedback](https://help.productfruits.com/en/article/server-api-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentInfo.userAgent` | body | `string` | no | User agent string of the submitter device. |
| `text` | body | `string` | yes | Feedback text. |
| `username` | body | `string` | yes | Username of the user submitting feedback. |
