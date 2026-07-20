# Intruder: List Target API Schemas



```
GET https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-target-api-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intruder `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-target-api-schemas?connectionId=$CONNECTION_ID&limit=25&offset=0&targetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "targetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intruder/latest/actions/list-target-api-schemas?${params}`, {
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
| `targetId` | string | yes | The Intruder target identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseUrl": "https://example.com",
      "id": 1,
      "name": "Ava Chen",
      "targetAuthenticationId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseUrl` | string |  |
| `id` | number |  |
| `name` | string |  |
| `targetAuthenticationId` | number |  |

## Native endpoint

Through the native Intruder API, this operation is `GET /targets/:target_id/api_schemas/` (base URL `https://api.intruder.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-target-api-schemas.md) for the provider-specific parameters and requirements.

