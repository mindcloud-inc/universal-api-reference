# Are.na: Move Connection

Moves a connection within a channel in Are.na.

```
PUT https://connect.mindcloud.co/v1/universal/are-na/latest/actions/move-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/move-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/move-connection', {
  method: 'PUT',
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
| `id` | string | no | Are.na connection ID. |
| `movement` | string | no | Movement strategy, e.g. insert_at. |
| `position` | number | no | Target position, 1-indexed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "metadata": {},
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `metadata` | object |  |
| `position` | number |  |

## Native endpoint

Through the native Are.na API, this operation is `POST connections/:id/move` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-connection.md) for the provider-specific parameters and requirements.

