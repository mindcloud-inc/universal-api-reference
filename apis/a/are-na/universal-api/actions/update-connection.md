# Are.na: Update Connection

Updates an existing connection in Are.na.

```
PUT https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/update-connection', {
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
| `metadata` | object | no | Metadata object to merge into the connection. |

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

Through the native Are.na API, this operation is `PUT connections/:id` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-connection.md) for the provider-specific parameters and requirements.

