# Create Access Token with PostcardMania

Creates a new access token in PostcardMania.

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/login`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Create Access Token](https://docs.pcmintegrations.com/docs/directmail-api/ffef03a112bb0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apiKey` | body | `string` | yes | Raw PCM portal API key. |
| `apiSecret` | body | `string` | yes | Raw PCM portal API secret. |
| `childRefNbr` | body | `string` | no | Optional child app account reference. |
