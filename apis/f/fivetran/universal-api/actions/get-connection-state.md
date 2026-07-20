# Fivetran: Get Connection State

Retrieves sync state for a connection in Fivetran.

```
GET https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-connection-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-connection-state?connectionId=$CONNECTION_ID&connectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/get-connection-state?${params}`, {
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
| `connectionId` | string | yes | The unique identifier for the connection within Fivetran. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "schema": {},
      "status": {},
      "table": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `schema` | object |  |
| `status` | object |  |
| `table` | object |  |

## Native endpoint

Through the native Fivetran API, this operation is `GET /connections/[:connectionId]/state` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection-state.md) for the provider-specific parameters and requirements.

