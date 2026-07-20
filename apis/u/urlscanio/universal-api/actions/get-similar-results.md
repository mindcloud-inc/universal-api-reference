# urlscan.io: Get Similar Results



```
GET https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-similar-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-similar-results?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/get-similar-results?${params}`, {
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
| `scanId` | string | no | The scan UUID to compare for similar results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "results": [
        {}
      ],
      "took": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `results` | array<object> |  |
| `took` | number |  |
| `total` | number |  |

## Native endpoint

Through the native urlscan.io API, this operation is `GET /api/v1/pro/result/{scanId}/similar/` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-similar-results.md) for the provider-specific parameters and requirements.

