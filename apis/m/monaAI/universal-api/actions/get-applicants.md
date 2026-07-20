# Mona AI: Get Applicants

Retrieves applicants from Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-applicants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-applicants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-applicants?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | object | no | Optional applicant filters such as jobId and status. |
| `limit` | number | no | Maximum applicants to return. |
| `page` | number | no | Page number to retrieve. |
| `sort` | object | no | Optional sort object with field and direction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pagination": {
        "nextPageToken": "string",
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Applicant records returned by Mona. |
| `pagination` | object | Pagination metadata for applicant results. |
| `pagination.nextPageToken` | string | Token for the next applicant page when available. |
| `pagination.total` | number | Total number of applicant records available. |

## Native endpoint

Through the native Mona AI API, this operation is `POST /database/getApplicantsFromDatabase` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-applicants.md) for the provider-specific parameters and requirements.

