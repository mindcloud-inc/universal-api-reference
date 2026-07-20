# Localazy: List Import Formats

Retrieves supported import formats from Localazy.

```
GET https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-import-formats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-import-formats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-import-formats?${params}`, {
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
      "arrays": [
        {}
      ],
      "keyTransformers": [
        {}
      ],
      "name": "Ava Chen",
      "plurals": [
        {}
      ],
      "supportArrays": true,
      "supportPlurals": true,
      "supportStrings": true,
      "supportStructuredKeys": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arrays` | array<object> | Supported array output modes when available. |
| `keyTransformers` | array<object> | Supported key-flattening strategies when available. |
| `name` | string | Human-readable format label. |
| `plurals` | array<object> | Supported plural output modes when available. |
| `supportArrays` | boolean | Whether the format supports string arrays. |
| `supportPlurals` | boolean | Whether the format supports plural forms. |
| `supportStrings` | boolean | Whether the format supports string values. |
| `supportStructuredKeys` | boolean | Whether the format supports nested keys. |
| `type` | string | Localazy import format type key. |

## Native endpoint

Through the native Localazy API, this operation is `GET /import/formats` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-import-formats.md) for the provider-specific parameters and requirements.

