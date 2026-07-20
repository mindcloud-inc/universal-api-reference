# Find Business Email with EmailVerify.io

Finds a business email in EmailVerify.io by name and domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/finder`
- **Base URL:** `https://app.emailverify.io/api/v1`
- **Official documentation:** [Find Business Email](https://www.emailverify.io/api/docs/#finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | Person's name to search for on the target domain. |
| `domain` | query | `string` | yes | Company domain to search for. |
