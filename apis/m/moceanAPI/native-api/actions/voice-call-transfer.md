# Voice Call Transfer with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22dial%22%2C%22to%22%3A%2260123456789%22%7D%5D`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Voice Call Transfer](https://moceanapi.com/docs#make-an-outbound-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-to` | query | `string` | yes | Phone number to call, including country code. |
