# Beebole: Activate a Subproject

Activates a subproject in Beebole.

```
PUT https://connect.mindcloud.co/v1/universal/beebole/latest/actions/activate-a-subproject
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/activate-a-subproject" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beebole/latest/actions/activate-a-subproject', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/activate-a-subproject.md) for the provider-specific parameters and requirements.

