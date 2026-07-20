# Voice Call Collect Digits with Mocean API

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/2/voice/dial?mocean-resp-format=json&mocean-command=%5B%7B%22action%22%3A%22say%22%2C%22text%22%3A%22Press%201%20to%20continue%22%2C%22language%22%3A%22en-US%22%7D%2C%7B%22action%22%3A%22collect%22%2C%22eventUrl%22%3A%5B%22https%3A%2F%2Fexample.com%2Fcollect%22%5D%7D%5D`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Voice Call Collect Digits](https://moceanapi.com/docs#make-an-outbound-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-to` | query | `string` | yes | Phone number to call, including country code. |
