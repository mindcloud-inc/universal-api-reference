# Create 2FA Application with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/2fa/2/applications`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Create 2FA Application](https://www.infobip.com/docs/api/platform/2fa/2fa-configuration/create-2fa-application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `configuration` | body | `object` | no | — |
| `configuration.allowMultiplePinVerifications` | body | `boolean` | no | Indicates whether multiple PIN verification is allowed. |
| `configuration.pinAttempts` | body | `number` | no | Number of possible PIN attempts. |
| `configuration.pinTimeToLive` | body | `string` | no | Validity period of PIN in specified time unit. Required format: `{timeLength}{timeUnit}`. `timeLength` is optional with a default value of 1. `timeUnit` can be set to: `ms`, `s`, `m`, `h` or `d` representing milliseconds, seconds, minutes, hours, and days respectively. Must not exceed one year, although much lower value is recommended. |
| `configuration.sendPinPerApplicationLimit` | body | `string` | no | Overall number of requests over a specified time period for generating a PIN and sending a message using a single application. Required format: `{attempts}/{timeLength}{timeUnit}`. `attempts` and `timeunit` are mandatory and `timeLength` is optional with a default value of 1. `timeUnit` is one of: `ms`, `s`, `m`, `h` or `d` representing milliseconds, seconds, minutes, hours, and days respectively. Must not exceed one year, although much lower value is recommended. |
| `configuration.sendPinPerPhoneNumberLimit` | body | `string` | no | Number of requests over a specified time period for generating a PIN and sending a message to one destination. Required format: `{attempts}/{timeLength}{timeUnit}`. `attempts` and `timeunit` are mandatory and `timeLength` is optional with a default value of 1. `timeUnit` is one of: `ms`, `s`, `m`, `h` or `d` representing milliseconds, seconds, minutes, hours, and days respectively. Must not exceed one year, although much lower value is recommended. |
| `configuration.verifyPinLimit` | body | `string` | no | The number of PIN verification requests over a specififed time period from one phone number (MSISDN). Required format: `{attempts}/{timeLength}{timeUnit}`. `attempts` and `timeunit` are mandatory and `timeLength` is optional with a default value of 1. `timeUnit` is one of: `ms`, `s`, `m`, `h` or `d` representing milliseconds, seconds, minutes, hours, and days respectively. Must not exceed one day, although much lower value is recommended. |
| `enabled` | body | `boolean` | no | Indicates whether the created application is enabled. |
| `name` | body | `string` | yes | 2FA application name. |
