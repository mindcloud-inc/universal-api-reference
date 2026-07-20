# Camio: Create Pinned Query

Creates a pinned query in Camio.

```
POST https://connect.mindcloud.co/v1/universal/camio/latest/actions/create-pinned-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/camio/latest/actions/create-pinned-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/camio/latest/actions/create-pinned-query', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | A unique id for the pinned query. |
| `text` | string | yes | The pinned Camio query text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "query": {},
      "serverName": "Ava Chen",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The pinned query id. |
| `query` | object | The parsed Camio query object. |
| `serverName` | string | The server name that accepted the pinned query. |
| `text` | string | The pinned query text. |

## Native endpoint

Through the native Camio API, this operation is `PUT /users/:user/queries/pinned` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pinned-query.md) for the provider-specific parameters and requirements.

