# Port API AI: Get Migration

Retrieves a migration from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-migration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-migration?connectionId=$CONNECTION_ID&migrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "migrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-migration?${params}`, {
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
| `migrationId` | string | yes | The Port migration identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "migration": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `migration` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /migrations/:migration_id` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-migration.md) for the provider-specific parameters and requirements.

