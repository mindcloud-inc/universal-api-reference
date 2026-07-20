# Update account with Kameleoon

## Endpoint

- **Method:** `PATCH`
- **Path:** `accounts/:accountId`
- **Base URL:** `https://api.kameleoon.com`
- **Official documentation:** [Update account](https://developers.kameleoon.com/apis/automation-api-rest/all-endpoints/partial-update-account/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Account identifier from Kameleoon. |
| `email` | body | `string` | no | Updated email for the account. |
| `firstName` | body | `string` | no | Updated first name. |
| `lastName` | body | `string` | no | Updated last name. |
| `password` | body | `string` | no | Updated password. |
| `passwordConfirm` | body | `string` | no | Password confirmation when changing password. |
| `preferredLocale` | body | `string` | no | Preferred locale: fr, en, or de. |
| `status` | body | `string` | no | Account status value. |
