# Erase.bg: Get Default Asset For Playground

Retrieves the default playground asset from Erase.bg.

```
GET https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-default-asset-for-playground
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Erase.bg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-default-asset-for-playground?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/erasebg/latest/actions/get-default-asset-for-playground?${params}`, {
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
      "_id": "string",
      "access": "string",
      "assetType": "string",
      "context": {},
      "fileId": "string",
      "format": "string",
      "height": 1,
      "isActive": true,
      "isOriginal": true,
      "kvStore": [
        {}
      ],
      "meta": {},
      "metadata": {},
      "name": "Ava Chen",
      "orgId": 1,
      "path": "string",
      "size": 1,
      "tags": [
        "string"
      ],
      "type": "string",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `access` | string |  |
| `assetType` | string |  |
| `context` | object |  |
| `fileId` | string |  |
| `format` | string |  |
| `height` | number |  |
| `isActive` | boolean |  |
| `isOriginal` | boolean |  |
| `kvStore` | array<object> |  |
| `meta` | object |  |
| `metadata` | object |  |
| `name` | string |  |
| `orgId` | number |  |
| `path` | string |  |
| `size` | number |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Erase.bg API, this operation is `GET /service/platform/assets/v1.0/playground/default` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-asset-for-playground.md) for the provider-specific parameters and requirements.

