# InsightIQ: Get Async Creator Profile Analytics

Retrieves an async creator analytics result from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-async-creator-profile-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-async-creator-profile-analytics?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-async-creator-profile-analytics?${params}`, {
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
| `id` | string | yes | InsightIQ job ID for the async profile analytics request |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "id": "string",
      "is_part_of_creator_list": true,
      "price_explanations": [
        {}
      ],
      "pricing": {},
      "profile": {},
      "status": "string",
      "work_platform": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object |  |
| `id` | string |  |
| `is_part_of_creator_list` | boolean |  |
| `price_explanations` | array<object> |  |
| `pricing` | object |  |
| `profile` | object |  |
| `status` | string |  |
| `work_platform` | object |  |

## Native endpoint

Through the native InsightIQ API, this operation is `GET /v1/social/creators/async/profiles/analytics/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-creator-profile-analytics.md) for the provider-specific parameters and requirements.

