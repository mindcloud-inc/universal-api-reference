# Keywords AI: List Testsets

Retrieves testset records from Keywords AI.

```
GET https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/list-testsets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keywords AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/list-testsets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keywordsAI/latest/actions/list-testsets?${params}`, {
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
      "testset_unique_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `testset_unique_id` | string |  |

## Native endpoint

Through the native Keywords AI API, this operation is `POST /api/testsets/list/` (base URL `https://api.respan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-testsets.md) for the provider-specific parameters and requirements.

