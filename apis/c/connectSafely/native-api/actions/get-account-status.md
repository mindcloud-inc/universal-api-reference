# Get account status with ConnectSafely

Retrieve the current status of a LinkedIn account. If accountId is provided, returns that specific account. Otherwise returns the most recently used account for the authenticated user.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/status`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get account status](https://connectsafely.ai/docs/api/linkedin-account/get-account-status-get-account-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | Optional LinkedIn account ID. If omitted, returns the most recently used account. |

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

`401`, `404`. Bodies follow the shared `{ success, code, message }` error shape.
