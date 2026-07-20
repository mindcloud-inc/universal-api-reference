# Update MFA Configuration with Frontegg

Updates MFA configuration for your Frontegg environment.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/configurations/v1/mfa`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Update MFA Configuration](https://developers.frontegg.com/ciam/api/identity/mfa-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authenticationApp.active` | body | `boolean` | yes | Whether authenticator app MFA is active. |
| `authenticationApp.serviceName` | body | `string` | yes | Authenticator app service name. |
| `sms.active` | body | `boolean` | yes | Whether SMS MFA is active. |
| `sms.tokenLifetimeSeconds` | body | `number` | yes | SMS MFA token lifetime in seconds. |
| `email.active` | body | `boolean` | yes | Whether email MFA is active. |
| `email.tokenLifetimeSeconds` | body | `number` | yes | Email MFA token lifetime in seconds. |
| `email.sender` | body | `string` | yes | Email MFA sender address. |
