# Typesense: Voice Multi Search

Finds results in Typesense using voice query search.

```
GET https://connect.mindcloud.co/v1/universal/typesense/latest/actions/voice-multi-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/voice-multi-search?connectionId=$CONNECTION_ID&searches=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searches": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/voice-multi-search?${params}`, {
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
| `searches` | object | yes | Voice multi-search request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "found": 1,
      "hits": [
        {}
      ],
      "response": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `found` | number |  |
| `hits` | array<object> |  |
| `response` | object |  |
| `results` | array<object> |  |

## Native endpoint

Through the native Typesense API, this operation is `POST /multi_search` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/voice-multi-search.md) for the provider-specific parameters and requirements.

