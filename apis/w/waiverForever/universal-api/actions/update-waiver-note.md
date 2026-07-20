# WaiverForever: Update Waiver Note

Updates a waiver note in WaiverForever.

```
PUT https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/update-waiver-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/update-waiver-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "note": "string",
  "waiverId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/update-waiver-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "note": "string",
    "waiverId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | yes | Updated waiver note text. |
| `waiverId` | string | yes | Signed waiver identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Provider response message. |
| `result` | boolean | Whether the waiver note update succeeded. |

## Native endpoint

Through the native WaiverForever API, this operation is `POST /openapi/v1/waiver/:waiver_id/note` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-waiver-note.md) for the provider-specific parameters and requirements.

