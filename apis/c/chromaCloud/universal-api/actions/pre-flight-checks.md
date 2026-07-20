# Chroma Cloud: Pre-flight checks

Retrieves pre-flight checks from Chroma Cloud.

```
GET https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/pre-flight-checks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/pre-flight-checks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/pre-flight-checks?${params}`, {
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
      "max_batch_size": 1,
      "supports_base64_encoding": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `max_batch_size` | number |  |
| `supports_base64_encoding` | boolean |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `GET /api/v2/pre-flight-checks` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pre-flight-checks.md) for the provider-specific parameters and requirements.

