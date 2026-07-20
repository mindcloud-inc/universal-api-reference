# SIGNL4: Update Event Source

Updates an event source in SIGNL4.

```
PUT https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-event-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-event-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventSourceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-event-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventSourceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventSourceId` | string | yes | ID of event source |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `description` | string | no |  |
| `teamId` | string | no |  |
| `disabled` | boolean | no |  |
| `options` | number | no | <p/><ul><li>0 = None</li><li>1 = DisableContentParsing</li></ul> |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "description": "string",
      "disabled": true,
      "groupId": "string",
      "id": "string",
      "lastEvent": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "options": 1,
      "subscriptionId": "string",
      "subType": "string",
      "teamId": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `groupId` | string |  |
| `id` | string |  |
| `lastEvent` | date |  |
| `name` | string |  |
| `options` | number |  |
| `subscriptionId` | string |  |
| `subType` | string |  |
| `teamId` | string |  |
| `type` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `PUT /v2/eventsources/{eventSourceId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event-source.md) for the provider-specific parameters and requirements.

