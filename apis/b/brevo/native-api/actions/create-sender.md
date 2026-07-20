# Create Sender with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/senders`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Create Sender](https://developers.brevo.com/reference/createsender)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The sender email address to verify and use. |
| `name` | body | `string` | yes | The sender display name. |
