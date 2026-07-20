# Voice Call Say Message with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22say%22%2C%22text%22%3A%22Hello%20from%20MindCloud%22%2C%22language%22%3A%22en-US%22%7D%5D`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Voice Call Say Message](https://moceanapi.com/docs#make-an-outbound-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-to` | query | `string` | yes | Phone number to call, including country code. |
