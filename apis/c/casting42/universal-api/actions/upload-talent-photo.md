# Casting42: Upload Talent Photo

Uploads a photo for a Casting42 talent.

```
POST https://connect.mindcloud.co/v1/universal/casting42/latest/actions/upload-talent-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/upload-talent-photo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/casting42/latest/actions/upload-talent-photo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentLabel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "isProfilePicture": true,
      "tag": "string",
      "talentTag": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentLabel` | string | Attachment label. |
| `createdAt` | date | Upload timestamp. |
| `filename` | string | Uploaded photo filename. |
| `isProfilePicture` | boolean | Whether the photo is marked as the profile picture. |
| `tag` | string | Photo tag. |
| `talentTag` | string | Related talent tag. |
| `url` | string | Uploaded photo URL. |

## Native endpoint

Through the native Casting42 API, this operation is `POST /talents/upload-photo` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-talent-photo.md) for the provider-specific parameters and requirements.

