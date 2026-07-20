# Are.na: Get Connection

Retrieves a connection by ID from Are.na.

```
GET https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/are-na/latest/actions/get-connection?${params}`, {
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
| `id` | string | no | Are.na connection ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {},
      "connectable": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | object |  |
| `connectable` | object |  |
| `created_at` | date |  |
| `id` | number |  |
| `position` | number |  |

## Native endpoint

Through the native Are.na API, this operation is `GET connections/:id` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection.md) for the provider-specific parameters and requirements.

