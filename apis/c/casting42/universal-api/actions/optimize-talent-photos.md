# Casting42: Optimize Talent Photos

Optimizes photos for a Casting42 talent.

```
PUT https://connect.mindcloud.co/v1/universal/casting42/latest/actions/optimize-talent-photos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/optimize-talent-photos" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "talentTag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/casting42/latest/actions/optimize-talent-photos', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "talentTag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `talentTag` | string | yes | Unique tag of the talent whose photos should be optimized. |

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
| `createdAt` | date | Photo creation timestamp. |
| `filename` | string | Photo filename. |
| `isProfilePicture` | boolean | Whether the photo is marked as the profile picture. |
| `tag` | string | Photo tag. |
| `talentTag` | string | Related talent tag. |
| `url` | string | Photo download URL. |

## Native endpoint

Through the native Casting42 API, this operation is `GET /api/v2/talents/optimize-photos-of-talent/{{talentTag}}` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/optimize-talent-photos.md) for the provider-specific parameters and requirements.

