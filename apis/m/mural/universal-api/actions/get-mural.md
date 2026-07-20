# Mural: Get Mural

Retrieves a mural from Mural by ID.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-mural
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-mural?connectionId=$CONNECTION_ID&muralId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "muralId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-mural?${params}`, {
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
| `muralId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_canvasLink": "https://example.com",
      "backgroundColor": "string",
      "createdBy": {},
      "createdOn": 1,
      "embedLink": "https://example.com",
      "favorite": true,
      "folderId": "string",
      "height": 1,
      "id": "string",
      "infinite": true,
      "roomId": 1,
      "sharingSettings": {},
      "state": "string",
      "status": "string",
      "thumbnailUrl": "https://example.com",
      "timerSoundTheme": "string",
      "title": "string",
      "updatedBy": {},
      "updatedOn": 1,
      "visitorAvatarTheme": "string",
      "visitorsSettings": {},
      "width": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_canvasLink` | string |  |
| `backgroundColor` | string |  |
| `createdBy` | object |  |
| `createdOn` | number |  |
| `embedLink` | string |  |
| `favorite` | boolean |  |
| `folderId` | string |  |
| `height` | number |  |
| `id` | string |  |
| `infinite` | boolean |  |
| `roomId` | number |  |
| `sharingSettings` | object |  |
| `state` | string |  |
| `status` | string |  |
| `thumbnailUrl` | string |  |
| `timerSoundTheme` | string |  |
| `title` | string |  |
| `updatedBy` | object |  |
| `updatedOn` | number |  |
| `visitorAvatarTheme` | string |  |
| `visitorsSettings` | object |  |
| `width` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Mural API, this operation is `GET /murals/:muralId` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mural.md) for the provider-specific parameters and requirements.

