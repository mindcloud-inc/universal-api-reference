# Topia: Get Dropped Asset by Unique Name

Finds a dropped asset in Topia by unique name.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-dropped-asset-by-unique-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-dropped-asset-by-unique-name?connectionId=$CONNECTION_ID&urlSlug=https%3A%2F%2Fexample.com&uniqueName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlSlug": "https://example.com",
  "uniqueName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-dropped-asset-by-unique-name?${params}`, {
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
| `uniqueName` | string | yes | Unique name assigned to the dropped asset. |

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

Through the native Topia API, this operation is `GET /v1/world/:urlSlug/asset-by-unique-name/:uniqueName` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dropped-asset-by-unique-name.md) for the provider-specific parameters and requirements.

