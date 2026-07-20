# Fivetran: Re-sync Connection

Starts a re-sync for a connection in Fivetran.

```
PUT https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/resync-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/resync-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/resync-connection', {
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
| `connectionId` | string | yes | The unique identifier for the connection within Fivetran. |
| `scope` | object | no | Optional map of schemas and tables to re-sync. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `POST /connections/[:connectionId]/resync` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resync-connection.md) for the provider-specific parameters and requirements.

