# Topia: List Avatars

Retrieves available avatars from Topia.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-avatars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-avatars?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/list-avatars?${params}`, {
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
| `profileId` | string | yes | Identifier for the profile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableFor": [
        "string"
      ],
      "canUseColors": true,
      "colors": [
        "string"
      ],
      "dancePreviewImage": "string",
      "emotePreviewImage": "string",
      "expressions": [
        "string"
      ],
      "id": "string",
      "isLive": true,
      "name": "Ava Chen",
      "previewImage": "string",
      "sitPreviewImage": "string",
      "spriteSheetId": "string",
      "standPreviewImage": "string",
      "transportPreviewImage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableFor` | array<string> |  |
| `canUseColors` | boolean |  |
| `colors` | array |  |
| `dancePreviewImage` | string |  |
| `emotePreviewImage` | string |  |
| `expressions` | array |  |
| `id` | string |  |
| `isLive` | boolean |  |
| `name` | string |  |
| `previewImage` | string |  |
| `sitPreviewImage` | string |  |
| `spriteSheetId` | string |  |
| `standPreviewImage` | string |  |
| `transportPreviewImage` | string |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/avatars/:profileId` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-avatars.md) for the provider-specific parameters and requirements.

