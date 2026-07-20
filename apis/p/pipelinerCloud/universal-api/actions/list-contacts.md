# Pipeliner Cloud: List Contacts

Retrieves contacts from Pipeliner Cloud.

```
GET https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeliner Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-contacts?${params}`, {
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
| `includeDeleted` | boolean | no | Include deleted records in the result set. |
| `expand` | string | no | Comma-separated related resources to expand. |
| `loadOnly` | string | no | Comma-separated fields to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formatted_name": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formatted_name` | string | Pipeliner contact display name. |
| `id` | string | Pipeliner contact ID. |

## Native endpoint

Through the native Pipeliner Cloud API, this operation is `GET /entities/Contacts` (base URL `{{credentials.serviceUrl}}/api/v100/rest/spaces/{{credentials.spaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

