# Get account premium status with ConnectSafely

Retrieve the premium subscription status of a LinkedIn account. Checks Sales Navigator license first via Identity API, then falls back to feature access API for other premium types (Recruiter, Business Premium). Returns premium type and access flags.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/:accountId/premium`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get account premium status](https://connectsafely.ai/docs/api/linkedin-account/get-account-accountid-premium-get-account-premium-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | param | `string` | yes | Unique identifier for the LinkedIn account (24-character hex string) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the request was successful |
| `accountId` | `string` | Unique account identifier |
| `accountName` | `string` | Full name of the LinkedIn account owner |
| `premiumType` | `list` | Type of premium subscription |
| `isPremium` | `boolean` | Whether the account has any premium subscription |
| `hasSalesNavigator` | `boolean` | Whether the account has Sales Navigator access |
| `hasRecruiter` | `boolean` | Whether the account has Recruiter access |
| `hasAwayMessages` | `boolean` | Whether the account can set away messages (Business Premium feature) |
| `hasAdvertiseBadge` | `boolean` | Whether the account has advertise badge access |
| `hasHiringManager` | `boolean` | Whether the account has hiring manager mailbox access |

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
