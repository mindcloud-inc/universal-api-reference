# Rocketadmin: Get Connection



```
GET https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-connection?connectionId=$CONNECTION_ID&connectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-connection?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connectionId` | string | yes | Rocketadmin connection identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "connection": {
        "database": "string",
        "host": "string",
        "id": "string",
        "port": 1,
        "title": "string",
        "type": "string",
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `connection` | object |  |
| `connection.database` | string |  |
| `connection.host` | string |  |
| `connection.id` | string |  |
| `connection.port` | number |  |
| `connection.title` | string |  |
| `connection.type` | string |  |
| `connection.username` | string |  |

## Native endpoint

Through the native Rocketadmin API, this operation is `GET /connection/one/:connectionId` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection.md) for the provider-specific parameters and requirements.

