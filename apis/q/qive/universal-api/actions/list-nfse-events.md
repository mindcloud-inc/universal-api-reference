# Qive: List NFSe Events



```
GET https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-nfse-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-nfse-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qive/latest/actions/list-nfse-events?${params}`, {
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
      "type": "string",
      "xml": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `type` | string |  |
| `xml` | string |  |

## Native endpoint

Through the native Qive API, this operation is `GET /v1/nfse/events` (base URL `https://sandbox-api.arquivei.com.br`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nfse-events.md) for the provider-specific parameters and requirements.

