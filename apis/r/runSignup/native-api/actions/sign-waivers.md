# Sign Waivers with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/participants/sign-waivers.json`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Sign Waivers](https://runsignup.com/API/v2/participants/sign-waivers.json/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | query | `number` | yes | Race ID. |
| `signed_waivers` | body | `string` | yes | — |
