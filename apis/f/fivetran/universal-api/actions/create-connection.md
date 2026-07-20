# Fivetran: Create Connection

Creates a new connection in your Fivetran account.

```
POST https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "service": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-connection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "service": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auth` | object | no | Connection authorization settings object when the connector supports API-based authorization. |
| `config` | object | no | Connection setup configuration object. |
| `groupId` | string | yes | The group ID where the connection belongs. |
| `paused` | boolean | no | Whether the connection is paused. |
| `service` | string | yes | The connector service type. |
| `syncFrequency` | number | no | The connection sync frequency in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `groupId` | string |  |
| `id` | string |  |
| `paused` | boolean |  |
| `schema` | string |  |
| `service` | string |  |
| `status` | object |  |

## Native endpoint

Through the native Fivetran API, this operation is `POST /connections` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-connection.md) for the provider-specific parameters and requirements.

