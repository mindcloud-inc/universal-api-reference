# Smartcar: Get Connection

Retrieves a connection from Smartcar.

```
GET https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/get-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/get-connection?connectionId=$CONNECTION_ID&connectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/get-connection?${params}`, {
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
| `connectionId` | string | yes | The unique identifier for the connection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Smartcar API, this operation is `GET /connections/:connectionId` (base URL `https://vehicle.api.smartcar.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection.md) for the provider-specific parameters and requirements.

