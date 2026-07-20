# Quire: Create Status

Creates a new status in Quire.

```
POST https://connect.mindcloud.co/v1/universal/quire/latest/actions/create-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quire/latest/actions/create-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quire/latest/actions/create-status', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen",
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
| `name` | string | yes | Display name of the new status. |
| `value` | number | yes | Unique numeric progress value for the new status. |
| `color` | string | no | Optional Quire color code such as 35. |

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

Through the native Quire API, this operation is `POST status/id/:projectId` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-status.md) for the provider-specific parameters and requirements.

