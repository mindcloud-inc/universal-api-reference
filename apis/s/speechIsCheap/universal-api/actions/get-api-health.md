# Speech is Cheap: Get API Health

Retrieves Speech is Cheap API health status.

```
GET https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/get-api-health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speech is Cheap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/get-api-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speechIsCheap/latest/actions/get-api-health?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Plain-text health response from the API. Runtime value was Healthy. |

## Native endpoint

Through the native Speech is Cheap API, this operation is `GET /jobs/health` (base URL `https://api.speechischeap.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-health.md) for the provider-specific parameters and requirements.

