# Powrbot: Get Search

Retrieves a bulk search job from Powrbot.

```
GET https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/get-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Powrbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/get-search?connectionId=$CONNECTION_ID&searchId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powrbot/latest/actions/get-search?${params}`, {
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
| `searchId` | number | yes | Numeric search job identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": [
        {}
      ],
      "company_count": 1,
      "count": 1,
      "count_completed": 1,
      "download_url": "https://example.com",
      "id": 1,
      "is_completed": true,
      "search_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | array<object> |  |
| `company_count` | number |  |
| `count` | number |  |
| `count_completed` | number |  |
| `download_url` | string |  |
| `id` | number |  |
| `is_completed` | boolean |  |
| `search_type` | string |  |

## Native endpoint

Through the native Powrbot API, this operation is `GET /search/:searchId/` (base URL `https://powrbot.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search.md) for the provider-specific parameters and requirements.

