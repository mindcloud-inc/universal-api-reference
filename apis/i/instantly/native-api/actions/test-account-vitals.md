# Test Account Vitals with Instantly

Retrieves account vitals test results from Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/accounts/test/vitals`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Test Account Vitals](https://developer.instantly.ai/api/v2/account/testaccountvitals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accounts[]` | body | `array<string>` | no | Email accounts to test. Send multiple values as a array. |
