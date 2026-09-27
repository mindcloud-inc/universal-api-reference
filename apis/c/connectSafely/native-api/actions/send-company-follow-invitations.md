# Send company follow invitations with ConnectSafely

Send invitations to LinkedIn users to follow a company page. This allows company page administrators to invite people to follow their company. Requires Super Admin access to the company page. Maximum 50 invitations per request.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:companyId/follow-invitations`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send company follow invitations](https://connectsafely.ai/docs/api/linkedin-profiles/post-organizations-companyid-follow-invitations-send-company-follow-invitations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | param | `string` | yes | LinkedIn company ID (numeric ID from organization URN) |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `companyId` | body | `string` | no | LinkedIn company ID (can also be specified in path) |
| `profileUrns` | body | `array` | yes | Array of LinkedIn profile URNs to invite (max 50 per request) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether at least one invitation was successful |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `companyId` | `string` | The company ID for which invitations were sent |
| `totalRequested` | `number` | Total number of invitations requested |
| `totalSuccessful` | `number` | Number of successful invitations |
| `totalFailed` | `number` | Number of failed invitations |
| `results` | `array` | Individual results for each invitation |
| `results[].profileUrn` | `string` | LinkedIn profile URN that was invited |
| `results[].success` | `boolean` | Whether the invitation was sent successfully |
| `results[].status` | `string` | Status of the invitation (e.g., "SENT", "FAILED") |
| `results[].error` | `string` | Error message if the invitation failed |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "companyId": "105672170",
  "totalRequested": 2,
  "totalSuccessful": 2,
  "totalFailed": 0,
  "results": [
    {
      "profileUrn": "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f...",
      "success": true,
      "status": "SENT"
    },
    {
      "profileUrn": "urn:li:fsd_profile:ACoAABJefVoBrz3XY4g...",
      "success": true,
      "status": "SENT"
    }
  ]
}
```

## Error status codes

`401`, `403`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
