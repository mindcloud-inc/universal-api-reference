# Apilio: Update Boolean Variable



```
PUT https://connect.mindcloud.co/v1/universal/apilio/latest/actions/update-boolean-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/apilio/latest/actions/update-boolean-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "a40f21df-7707-4898-9688-69bf1f8dd184",
  "value": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apilio/latest/actions/update-boolean-variable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "a40f21df-7707-4898-9688-69bf1f8dd184",
    "value": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | The UUID of the boolean variable to update. Default: `a40f21df-7707-4898-9688-69bf1f8dd184`. |
| `value` | boolean | yes | The new boolean value for the boolean variable. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |
| `value` | boolean |  |

## Native endpoint

Through the native Apilio API, this operation is `PUT /api/v1/boolean_variables/{{uuid}}` (base URL `https://api.apilio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-boolean-variable.md) for the provider-specific parameters and requirements.

