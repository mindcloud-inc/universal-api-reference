# Send Verify Code Telegram with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/verify/req/telegram?mocean-resp-format=json`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Send Verify Code Telegram](https://moceanapi.com/docs#send-code-over-telegram)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-brand` | query | `string` | yes | Brand or application name for the verification message. |
| `mocean-from` | query | `string` | yes | Telegram bot username. |
| `mocean-to` | query | `string` | yes | Telegram chat ID. |
