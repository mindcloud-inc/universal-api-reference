# Get specific account status with ConnectSafely

Retrieve the current status of a specific LinkedIn account by ID. Returns account details including name, public ID, operational status, session validity, and LinkedIn plan info (premium type). Useful for multi-account setups to check individual account status.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/:accountId/status`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get specific account status](https://connectsafely.ai/docs/api/linkedin-account/get-account-accountid-status-get-account-status-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | param | `string` | yes | Unique identifier for the LinkedIn account (24-character hex string) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | `string` | Unique account identifier |
| `firstName` | `string` | LinkedIn user first name |
| `lastName` | `string` | LinkedIn user last name |
| `publicId` | `string` | LinkedIn public profile ID (e.g., "john-doe-123") |
| `platform` | `string` | Platform name (e.g., "ConnectSafely") |
| `status` | `list` | Internal account operational status (AVAILABLE = available, IN_USE = busy, ERROR = needs attention) |
| `enabled` | `boolean` | Whether the account is enabled for automation |
| `lastUsed` | `date` | Last activity timestamp |
| `hasTokens` | `boolean` | Whether valid LinkedIn session tokens exist |
| `linkedinPlan` | `object` | LinkedIn premium plan info (only returned for accounts with AVAILABLE or WARMUP status, cached for 12 hours) |
| `linkedinPlan.premiumType` | `list` | Type of LinkedIn premium subscription |
| `linkedinPlan.isPremium` | `boolean` | Whether the account has any premium subscription |
| `linkedinPlan.hasSalesNavigator` | `boolean` | Has Sales Navigator access |
| `linkedinPlan.hasRecruiter` | `boolean` | Has Recruiter access |
| `linkedinPlan.hasAwayMessages` | `boolean` | Has away messages (Business Premium feature) |
| `linkedinPlan.hasAdvertiseBadge` | `boolean` | Has advertise badge access |
| `linkedinPlan.hasHiringManager` | `boolean` | Has hiring manager mailbox access |

## Error status codes

`400`, `401`, `404`. Bodies follow the shared `{ success, code, message }` error shape.
