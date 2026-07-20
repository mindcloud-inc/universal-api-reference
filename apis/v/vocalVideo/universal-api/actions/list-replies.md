# Vocal Video: List Replies

Retrieves reply samples from Vocal Video.

```
GET https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/list-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vocal Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/list-replies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/list-replies?${params}`, {
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
      "collector": {},
      "company_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_1": "string",
      "custom_2": "string",
      "custom_3": "string",
      "email": "ava@example.com",
      "id": 1,
      "job_title": "string",
      "name": "Ava Chen",
      "release_agreed": true,
      "responses": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collector` | object | Collector metadata. |
| `company_name` | string | Respondent company name. |
| `created_at` | date | Response creation timestamp. |
| `custom_1` | string | Custom field 1. |
| `custom_2` | string | Custom field 2. |
| `custom_3` | string | Custom field 3. |
| `email` | string | Respondent email. |
| `id` | number | Response id. |
| `job_title` | string | Respondent job title. |
| `name` | string | Respondent name. |
| `release_agreed` | boolean | Whether the release was agreed. |
| `responses` | array<object> | Submitted prompt responses. |
| `url` | string | Vocal Video app URL for the response. |

## Native endpoint

Through the native Vocal Video API, this operation is `GET /replies` (base URL `https://vocalvideo.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-replies.md) for the provider-specific parameters and requirements.

