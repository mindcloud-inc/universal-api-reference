# SIGNL4: Annotate Alert

Creates an annotation for an alert in SIGNL4.

```
POST https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/annotate-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/annotate-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "alertId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/annotate-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "alertId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alertId` | string | yes | Id of the alert to annotate. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | number | no | <p/><ul><li>0 = None</li><li>1 = Text</li><li>2 = Image</li></ul> |
| `text` | string | no |  |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "teamId": "string",
      "text": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "type": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `teamId` | string |  |
| `text` | string |  |
| `timestamp` | date |  |
| `type` | number |  |
| `userId` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `POST /v2/alerts/{alertId}/annotate` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/annotate-alert.md) for the provider-specific parameters and requirements.

