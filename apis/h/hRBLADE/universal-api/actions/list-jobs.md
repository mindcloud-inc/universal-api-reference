# HRBLADE: List Jobs



```
GET https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/list-jobs?${params}`, {
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
      "code": 1,
      "error": true,
      "response": {
        "data": [
          {
            "active": 1,
            "agencyId": 1,
            "companyId": 1,
            "createdAt": "2026-05-07T12:00:00.000Z",
            "description": "string",
            "hashLink": "https://example.com",
            "id": 1,
            "interviewedCount": 1,
            "invitedCount": 1,
            "language": "string",
            "name": "Ava Chen",
            "permissions": {
              "editJobs": true,
              "rateResponses": true
            },
            "previewVideo": "string",
            "startAt": "2026-05-07T12:00:00.000Z",
            "updatedAt": "2026-05-07T12:00:00.000Z"
          }
        ],
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Provider status code. |
| `error` | boolean | Error indicator. |
| `response.data[].active` | number | Job active flag (0/1). |
| `response.data[].agencyId` | number | Agency identifier. |
| `response.data[].companyId` | number | Company identifier. |
| `response.data[].createdAt` | date | Job creation timestamp. |
| `response.data[].description` | string | Job description. |
| `response.data[].hashLink` | string | Public hash link. |
| `response.data[].id` | number | Job identifier. |
| `response.data[].interviewedCount` | number | Interviewed candidate count. |
| `response.data[].invitedCount` | number | Invited candidate count. |
| `response.data[].language` | string | Job language code. |
| `response.data[].name` | string | Job name. |
| `response.data[].permissions.editJobs` | boolean | Permission to edit jobs. |
| `response.data[].permissions.rateResponses` | boolean | Permission to rate responses. |
| `response.data[].previewVideo` | string | Preview video URL. |
| `response.data[].startAt` | date | Job start timestamp. |
| `response.data[].updatedAt` | date | Job update timestamp. |
| `response.message` | string | Optional response message. |

## Native endpoint

Through the native HRBLADE API, this operation is `GET /jobs` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

