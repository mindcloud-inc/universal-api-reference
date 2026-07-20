# WorkOS: Get a Directory Group

Retrieves a directory group from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory-group?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory-group?${params}`, {
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
| `id` | string | yes | Unique identifier for the Directory Group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "directory_id": "string",
      "id": "string",
      "idp_id": "string",
      "message": "string",
      "name": "Ava Chen",
      "object": "string",
      "organization_id": "string",
      "raw_attributes": {},
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | An ISO 8601 timestamp. |
| `directory_id` | string | The identifier of the Directory the Directory Group belongs to. |
| `id` | string | Unique identifier for the Directory Group. |
| `idp_id` | string | Unique identifier for the group, assigned by the Directory Provider. Different Directory Providers use different ID formats. |
| `message` | string | WorkOS response field message. |
| `name` | string | The name of the Directory Group. |
| `object` | string | Distinguishes the Directory Group object. |
| `organization_id` | string | The identifier for the Organization in which the Directory resides. |
| `raw_attributes` | object | The raw attributes received from the directory provider. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /directory_groups/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-directory-group.md) for the provider-specific parameters and requirements.

