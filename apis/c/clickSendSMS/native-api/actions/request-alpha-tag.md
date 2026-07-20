# Request Alpha Tag with ClickSend SMS

Requests a new alpha tag in ClickSend SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/alpha-tags`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Request Alpha Tag](https://developers.clicksend.com/docs/messaging/sender_ids/alpha-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alpha_tag` | body | `string` | yes | Requested alpha sender tag. |
| `reason` | body | `string` | no | Business reason for requesting the tag. |
| `countries[]` | body | `array<string>` | no | ISO country codes where the tag will be used. |
| `businesses[]` | body | `array<object>` | no | Business metadata objects for approval. |
