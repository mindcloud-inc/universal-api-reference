# Check relationship status with profile with ConnectSafely

Check the relationship between your default LinkedIn account and a target profile. Returns connection status (1st, 2nd, 3rd degree), whether you follow them, and if you are connected. Useful for determining which actions are available (message, connect, etc.).

## Endpoint

- **Method:** `GET`
- **Path:** `/relationship/:profileId`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Check relationship status with profile](https://connectsafely.ai/docs/api/linkedin-actions/get-relationship-profileid-check-relationship)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | param | `string` | yes | LinkedIn profile vanity URL slug (the part after linkedin.com/in/, e.g., "john-doe-123") |

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
