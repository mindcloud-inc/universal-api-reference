# mintBlue: Create Event Listener

Creates a new event listener in mintBlue.

```
POST https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/create-event-listener
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mintBlue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/create-event-listener" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.name": "Ava Chen",
  "params.trigger.type": "string",
  "params.trigger.options": {},
  "params.actions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/create-event-listener', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.name": "Ava Chen",
    "params.trigger.type": "string",
    "params.trigger.options": {},
    "params.actions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.name` | string | yes | Event listener name. |
| `params.trigger.type` | string | yes | Trigger type. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.trigger.options` | object | yes | Trigger options object. For `mintblue.transaction.created`, include `project_id` and `txo`. |
| `params.actions[]` | array<object> | yes | Action definitions array. Use provider token `insert_into_project` (underscore) or `webhook`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "trigger": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `trigger` | object |  |

## Native endpoint

Through the native mintBlue API, this operation is `POST /sdk/latest` (base URL `https://api.mintblue.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-listener.md) for the provider-specific parameters and requirements.

