# PixieBrix: List Databases

Retrieves databases from a PixieBrix organization.

```
GET https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-databases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixieBrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-databases?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationPk=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationPk": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixieBrix/latest/actions/list-databases?${params}`, {
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
| `organizationPk` | string | yes | PixieBrix organization identifier. |
| `q` | string | no | Search text for narrowing database results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "enforce_schema": true,
      "id": "string",
      "last_write_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "num_records": 1,
      "organization_id": "string",
      "owner_field": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `enforce_schema` | boolean |  |
| `id` | string |  |
| `last_write_at` | date |  |
| `name` | string |  |
| `num_records` | number |  |
| `organization_id` | string |  |
| `owner_field` | string |  |
| `type` | string |  |

## Native endpoint

Through the native PixieBrix API, this operation is `GET /api/organizations/:organization_pk/databases/` (base URL `https://app.pixiebrix.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-databases.md) for the provider-specific parameters and requirements.

