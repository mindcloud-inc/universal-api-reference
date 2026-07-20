# pixx.io: Create Upload Link

Creates a new upload link in your pixx.io workspace.

```
POST https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-upload-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-upload-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/create-upload-link', {
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
| `description` | string | no | The upload link description. |
| `directoryId` | number | no | The directory the upload link points to. |
| `name` | string | yes | The upload link name. |
| `validityPeriod` | string | no | How long the upload link remains valid. Default: `oneWeek`. |

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

Through the native pixx.io API, this operation is `POST /uploadLinks` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-upload-link.md) for the provider-specific parameters and requirements.

