# Quire: Update Status

Updates an existing status in Quire.

```
PUT https://connect.mindcloud.co/v1/universal/quire/latest/actions/update-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quire/latest/actions/update-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quire/latest/actions/update-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The project ID or shortcut, for example App_Account. |
| `value` | number | yes | Current numeric status value to update. |
| `name` | string | no | Optional updated display name for the status. |
| `newValue` | number | no | Optional replacement numeric progress value for the status. |
| `color` | string | no | Optional updated Quire color code such as 35. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "name": "Ava Chen",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `name` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Quire API, this operation is `PUT status/id/:projectId/:value` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-status.md) for the provider-specific parameters and requirements.

