# Topia: List Dropped Assets by Scene Drop ID

Retrieves dropped assets in Topia by scene drop ID.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-dropped-assets-by-scene-drop-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-dropped-assets-by-scene-drop-id?connectionId=$CONNECTION_ID&urlSlug=https%3A%2F%2Fexample.com&sceneDropId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlSlug": "https://example.com",
  "sceneDropId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-dropped-assets-by-scene-drop-id?${params}`, {
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
| `urlSlug` | string | yes | Topia world URL slug. |
| `sceneDropId` | string | yes | Identifier for the scene drop. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetId": "string",
      "assetName": "Ava Chen",
      "assetScale": 1,
      "bottomLayerURL": "https://example.com",
      "clickType": "string",
      "id": "string",
      "mediaLink": "https://example.com",
      "position": {},
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
| `assetId` | string |  |
| `assetName` | string |  |
| `assetScale` | number |  |
| `bottomLayerURL` | string |  |
| `clickType` | string |  |
| `id` | string |  |
| `mediaLink` | string |  |
| `position` | object |  |
| `specialType` | string |  |
| `topLayerURL` | string |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/world/:urlSlug/assets-with-scene-drop-id/:sceneDropId` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dropped-assets-by-scene-drop-id.md) for the provider-specific parameters and requirements.

