# SIGNL4: Create Event Source

Creates an event source in SIGNL4.

```
POST https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/create-event-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/create-event-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/create-event-source', {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | number | no | <p/><ul><li>0 = None</li><li>1 = Email</li><li>2 = Webhook</li></ul> |
| `name` | string | no |  |
| `description` | string | no |  |
| `teamId` | string | no |  |
| `disabled` | boolean | no |  |
| `language` | number | no | <p/><ul><li>0 = EN</li><li>1 = DE</li></ul> |
| `subType` | string | no |  |
| `targets[]` | array<object> | no |  |
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

Through the native SIGNL4 API, this operation is `POST /v2/eventsources` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-source.md) for the provider-specific parameters and requirements.

