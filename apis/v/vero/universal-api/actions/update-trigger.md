# Vero: Update Trigger

Updates an existing trigger in Vero.

```
PUT https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-trigger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-trigger" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "trigger_example"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vero/latest/actions/update-trigger', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "trigger_example"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The trigger identifier. Default: `trigger_example`. |
| `type` | string | no | Optional trigger type update. |
| `event` | object | no | Optional trigger event object update. |
| `schedule` | object | no | Optional trigger schedule object update. |
| `recurring` | boolean | no | Optional recurring flag update. |
| `immediate` | boolean | no | Optional immediate flag update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Trigger identifier. |
| `object` | string | Resource type. |
| `type` | string | Trigger type. |

## Native endpoint

Through the native Vero API, this operation is `PATCH /api/v4/triggers/:id` (base URL `https://api.getvero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-trigger.md) for the provider-specific parameters and requirements.

