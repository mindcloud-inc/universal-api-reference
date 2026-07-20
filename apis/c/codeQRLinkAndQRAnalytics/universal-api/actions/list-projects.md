# CodeQR - Link and QR Analytics: List Projects

Retrieves projects from CodeQR.

```
GET https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "conversionEnabled": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domains": [
        {}
      ],
      "domainsLimit": 1,
      "id": "string",
      "linksUsage": 1,
      "metadata": {},
      "name": "Ava Chen",
      "plan": "string",
      "qrCodesUsage": 1,
      "scans": 1,
      "slug": "string",
      "tagsLimit": 1,
      "trialEndDate": "2026-05-07T12:00:00.000Z",
      "trialStartDate": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "users": [
        {}
      ],
      "usersLimit": 1,
      "webhookEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `conversionEnabled` | boolean |  |
| `createdAt` | date |  |
| `domains` | array<object> |  |
| `domainsLimit` | number |  |
| `id` | string |  |
| `linksUsage` | number |  |
| `metadata` | object |  |
| `name` | string |  |
| `plan` | string |  |
| `qrCodesUsage` | number |  |
| `scans` | number |  |
| `slug` | string |  |
| `tagsLimit` | number |  |
| `trialEndDate` | date |  |
| `trialStartDate` | date |  |
| `updatedAt` | date |  |
| `users` | array<object> |  |
| `usersLimit` | number |  |
| `webhookEnabled` | boolean |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `GET /projects` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

