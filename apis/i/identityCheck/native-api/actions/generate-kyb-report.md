# Generate KYB Report with IdentityCheck

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/verification/namescan/kyb`
- **Base URL:** `https://identity.stackgo.io/api`
- **Official documentation:** [Generate KYB Report](https://stackgo.notion.site/How-to-Generate-an-IdentityCheck-API-Key-38a12805b43249a480a96b346c491740)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countryCode` | body | `string` | yes | Company registration country code. |
| `registrationCode` | body | `string` | yes | Company registration code. |
