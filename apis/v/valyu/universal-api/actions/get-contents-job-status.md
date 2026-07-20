# Valyu: Get Contents Job Status



```
GET https://connect.mindcloud.co/v1/universal/valyu/latest/actions/get-contents-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Valyu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/get-contents-job-status?connectionId=$CONNECTION_ID&job_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "job_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/valyu/latest/actions/get-contents-job-status?${params}`, {
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
| `job_id` | string | yes | The contents job ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "dataType": "string",
      "description": "string",
      "id": "string",
      "imageUrl": {},
      "length": 1,
      "navLinks": [
        {}
      ],
      "orgId": "string",
      "price": 1,
      "publicationDate": "2026-05-07T12:00:00.000Z",
      "source": "string",
      "sourceType": "string",
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `dataType` | string |  |
| `description` | string |  |
| `id` | string |  |
| `imageUrl` | object |  |
| `length` | number |  |
| `navLinks` | array<object> |  |
| `orgId` | string |  |
| `price` | number |  |
| `publicationDate` | date |  |
| `source` | string |  |
| `sourceType` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Valyu API, this operation is `GET /contents/jobs/:job_id` (base URL `https://api.valyu.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contents-job-status.md) for the provider-specific parameters and requirements.

