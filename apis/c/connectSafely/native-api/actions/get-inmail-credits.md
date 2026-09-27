# Get InMail credits with ConnectSafely

Get the InMail credits balance for a LinkedIn account. Automatically detects account type (Sales Navigator, Business Premium, Recruiter) and uses the appropriate API. Non-premium accounts return 0 credits.

## Endpoint

- **Method:** `GET`
- **Path:** `/inmail/credits`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get InMail credits](https://connectsafely.ai/docs/api/uncategorized/get-inmail-credits-get-inmail-credits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID. If omitted, uses the default account. |
| `debug` | query | `list` | no | Set to "true" to include raw API response in the result. Accepted values: `true`, `false`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `inMailCredits` | `number` | Available InMail credits |
| `totalCredits` | `number` | Total credits (Sales Navigator only) |
| `usedCredits` | `number` | Used credits (Sales Navigator only) |
| `entityUrn` | `string` | Entity URN for the credits |
| `accountId` | `string` | LinkedIn account ID used |
| `premiumType` | `list` | Premium account type |
| `message` | `string` | Additional info (e.g. for non-premium accounts) |

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
