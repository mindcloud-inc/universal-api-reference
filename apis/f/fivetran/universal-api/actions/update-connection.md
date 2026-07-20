# Fivetran: Update Connection

Updates an existing connection in your Fivetran account.

```
PUT https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auth` | object | no | Connection authorization settings object. |
| `config` | object | no | Connection setup configuration object. |
| `connectionId` | string | yes | The unique identifier for the connection within Fivetran. |
| `paused` | boolean | no | Whether the connection is paused. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "groupId": "string",
      "id": "string",
      "paused": true,
      "schema": "string",
      "service": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `groupId` | string |  |
| `id` | string |  |
| `paused` | boolean |  |
| `schema` | string |  |
| `service` | string |  |
| `status` | object |  |

## Native endpoint

Through the native Fivetran API, this operation is `PATCH /connections/[:connectionId]` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-connection.md) for the provider-specific parameters and requirements.

