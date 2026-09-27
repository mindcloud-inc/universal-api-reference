# Check relationship status with specific account with ConnectSafely

Check the relationship between a specific LinkedIn account and a target profile. Useful for multi-account setups to check relationships from different accounts. Returns connection degree, follow status, and connection status.

## Endpoint

- **Method:** `GET`
- **Path:** `/relationship/:accountId/:profileId`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Check relationship status with specific account](https://connectsafely.ai/docs/api/linkedin-actions/get-relationship-accountid-profileid-check-relationship-specific-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | param | `string` | yes | Unique identifier for the LinkedIn account to check from |
| `profileId` | param | `string` | yes | Target LinkedIn profile vanity URL slug (the part after linkedin.com/in/, e.g., "john-doe-123") |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connected` | `boolean` | Whether you are 1st-degree connected |
| `invitationSent` | `boolean` | Whether you have sent a connection invitation |
| `invitationReceived` | `boolean` | Whether you have received a connection invitation |
| `status` | `list` | Connection status |
| `profileUrn` | `string` | LinkedIn profile URN of the target user |
| `accountId` | `string` | LinkedIn account ID used for the check |

### Example response

```json
{
  "connected": false,
  "invitationSent": false,
  "invitationReceived": false,
  "status": "NOT_CONNECTED",
  "profileUrn": "urn:li:fsd_profile:ACoAAA24A-MBVEvT49xpVF2gnWrhvmUIPDJshSM",
  "accountId": "acc_12345"
}
```

## Error status codes

`404`. Bodies follow the shared `{ success, code, message }` error shape.
