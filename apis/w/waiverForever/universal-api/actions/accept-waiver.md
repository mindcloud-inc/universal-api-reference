# WaiverForever: Accept Waiver

Accepts a waiver in WaiverForever.

```
PUT https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/accept-waiver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/accept-waiver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "waiverId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/accept-waiver', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "waiverId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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
| `result` | boolean | Whether the accept request succeeded. |

## Native endpoint

Through the native WaiverForever API, this operation is `POST /openapi/v2/waiver/:waiver_id/accept` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accept-waiver.md) for the provider-specific parameters and requirements.

