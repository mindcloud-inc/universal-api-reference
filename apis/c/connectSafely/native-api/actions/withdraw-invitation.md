# Withdraw a sent connection invitation with ConnectSafely

Withdraws a pending connection invitation that was previously sent to a LinkedIn user. Only the profileId is required - other fields will be auto-fetched from the profile if not provided. The API will verify that a pending invitation exists before attempting withdrawal.

## Endpoint

- **Method:** `POST`
- **Path:** `/invitations/withdraw`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Withdraw a sent connection invitation](https://connectsafely.ai/docs/api/linkedin-actions/post-invitations-withdraw-withdraw-invitation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `profileId` | body | `string` | yes | LinkedIn profile vanity URL slug (the part after linkedin.com/in/) of the person whose invitation to withdraw. This is the only required field. |
| `memberId` | body | `string` | no | LinkedIn member ID (ACoAAA format). Optional - will be auto-fetched from profile if not provided. |
| `firstName` | body | `string` | no | First name of the person. Optional - will be auto-fetched from profile if not provided. |
| `lastName` | body | `string` | no | Last name of the person. Optional - will be auto-fetched from profile if not provided. |
| `profileUrn` | body | `string` | no | LinkedIn profile URN. Optional - will be auto-fetched from profile if not provided. |
| `invitationId` | body | `string` | no | LinkedIn invitation ID. Optional - will be auto-fetched from profile if not provided. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the withdrawal was successful |
| `message` | `string` | Success or error message |
| `accountId` | `string` | LinkedIn account ID used for the request |

### Example response

```json
{
  "success": true,
  "message": "Successfully withdrew invitation to John Doe",
  "accountId": "696ce9e780e0483585e4e553"
}
```

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
