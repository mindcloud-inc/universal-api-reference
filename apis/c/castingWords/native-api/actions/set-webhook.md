# Set Webhook with CastingWords

Updates webhook settings in CastingWords.

## Endpoint

- **Method:** `POST`
- **Path:** `webhook`
- **Base URL:** `https://castingwords.com/store/API4`
- **Official documentation:** [Set Webhook](https://castingwords.com/docs/developer/SimpleAPI.html#webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook` | body | `string` | yes | HTTP or HTTPS endpoint to receive CastingWords webhook events. |
