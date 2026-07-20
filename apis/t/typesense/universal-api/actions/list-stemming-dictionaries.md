# Typesense: List Stemming Dictionaries

Retrieves all stemming dictionaries from Typesense.

```
GET https://connect.mindcloud.co/v1/universal/typesense/latest/actions/list-stemming-dictionaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typesense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typesense/latest/actions/list-stemming-dictionaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typesense/latest/actions/list-stemming-dictionaries?${params}`, {
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
      "dictionaries": [
        {}
      ],
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dictionaries` | array<object> |  |
| `response` | object |  |

## Native endpoint

Through the native Typesense API, this operation is `GET /stemming/dictionaries` (base URL `https://5brh8vz1lictf0jop-1.a2.typesense.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stemming-dictionaries.md) for the provider-specific parameters and requirements.

