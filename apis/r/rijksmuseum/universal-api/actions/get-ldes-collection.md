# Rijksmuseum: Get LDES Collection



```
GET https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-ldes-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rijksmuseum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-ldes-collection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-ldes-collection?${params}`, {
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
      "@context": {},
      "@id": "string",
      "@type": "string",
      "timestampPath": {},
      "versionOfPath": {},
      "view": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | object |  |
| `@id` | string |  |
| `@type` | string |  |
| `timestampPath` | object |  |
| `versionOfPath` | object |  |
| `view` | object |  |

## Native endpoint

Through the native Rijksmuseum API, this operation is `GET /ldes/collection.json` (base URL `https://data.rijksmuseum.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ldes-collection.md) for the provider-specific parameters and requirements.

