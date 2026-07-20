# xMatters: Create a change record

Creates a change record in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-change-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-change-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-a-change-record', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `changedAt` | string | no |  |
| `changedBy` | string | no |  |
| `changeType` | string | no |  |
| `service` | string | no |  |
| `source` | string | no |  |
| `summary` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changedAt": "2026-05-07T12:00:00.000Z",
      "changedBy": "string",
      "changeType": "string",
      "id": "string",
      "service": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "source": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changedAt` | date |  |
| `changedBy` | string |  |
| `changeType` | string |  |
| `id` | string |  |
| `service.id` | string |  |
| `service.links.self` | string |  |
| `service.recipientType` | string |  |
| `service.targetName` | string |  |
| `source` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST changes` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-change-record.md) for the provider-specific parameters and requirements.

