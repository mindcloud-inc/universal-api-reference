# pixx.io: Create External Share

Creates a new external share in your pixx.io workspace.

```
POST https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-external-share
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-external-share" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-external-share', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | number | no | Collection ID to share. |
| `fileIds` | number<number> | no | File IDs to share. Accepts multiple values as an array. |
| `name` | string | yes | The external share name. |
| `validityPeriod` | string | no | The duration until the share link expires. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "shareKey": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `shareKey` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `POST /externalShares` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-external-share.md) for the provider-specific parameters and requirements.

