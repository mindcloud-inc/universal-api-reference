# Mural: Duplicate Mural

Creates a new mural in Mural by duplicating another mural.

```
POST https://connect.mindcloud.co/v1/universal/mural/latest/actions/duplicate-mural
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mural/latest/actions/duplicate-mural" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "muralId": "string",
  "roomId": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mural/latest/actions/duplicate-mural', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "muralId": "string",
    "roomId": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `muralId` | string | yes |  |
| `roomId` | number | yes |  |
| `title` | string | yes |  |
| `folderId` | string | no |  |
| `infinite` | boolean | no |  |

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

Through the native Mural API, this operation is `POST /murals/:muralId/duplicate` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-mural.md) for the provider-specific parameters and requirements.

