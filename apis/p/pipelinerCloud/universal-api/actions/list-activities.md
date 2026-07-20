# Pipeliner Cloud: List Activities

Retrieves activities from Pipeliner Cloud.

```
GET https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeliner Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelinerCloud/latest/actions/list-activities?${params}`, {
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
      "id": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Pipeliner activity ID. |
| `subject` | string | Pipeliner activity subject. |

## Native endpoint

Through the native Pipeliner Cloud API, this operation is `GET /entities/Activities` (base URL `{{credentials.serviceUrl}}/api/v100/rest/spaces/{{credentials.spaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

