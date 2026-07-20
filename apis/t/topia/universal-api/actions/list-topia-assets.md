# Topia: List Topia Assets

Retrieves Topia-provided assets from the shared library.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-topia-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-topia-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-topia-assets?${params}`, {
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
      "addedOn": "2026-05-07T12:00:00.000Z",
      "assetName": "Ava Chen",
      "bottomLayerURL": "https://example.com",
      "id": "string",
      "isPublic": true,
      "library": "string",
      "platformAsset": true,
      "specialType": "string",
      "topLayerURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedOn` | date |  |
| `assetName` | string |  |
| `bottomLayerURL` | string |  |
| `id` | string |  |
| `isPublic` | boolean |  |
| `library` | string |  |
| `platformAsset` | boolean |  |
| `specialType` | string |  |
| `topLayerURL` | string |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/assets/topia-assets` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-topia-assets.md) for the provider-specific parameters and requirements.

