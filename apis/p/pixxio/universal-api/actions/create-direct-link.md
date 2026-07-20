# pixx.io: Create Direct Link

Creates a new direct link in your pixx.io workspace.

```
POST https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-direct-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-direct-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": 1,
  "fileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-direct-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": 1,
    "fileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `downloadType` | string | no | Download type such as original, preview, custom, or downloadFormat. Default: `original`. |
| `fileExtension` | string | no | Output file extension when using custom conversion settings. Default: `jpg`. |
| `fileId` | number | yes | The file ID for the direct link. |
| `fileName` | string | yes | The direct link file name without file extension. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directLinkID": 1,
      "downloadURL": "https://example.com",
      "fileExtension": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directLinkID` | number |  |
| `downloadURL` | string |  |
| `fileExtension` | string |  |
| `fileName` | string |  |
| `fileSize` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `POST /directLinks` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-direct-link.md) for the provider-specific parameters and requirements.

