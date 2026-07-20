# WorkOS: Get a Directory

Retrieves a directory from your WorkOS environment.

```
GET https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workOS/latest/actions/get-a-directory?${params}`, {
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
| `id` | string | yes | Unique identifier for the Directory. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "external_key": "string",
      "id": "string",
      "message": "string",
      "metadata": {},
      "name": "Ava Chen",
      "object": "string",
      "organization_id": "string",
      "state": "string",
      "type": "string",
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
| `domain` | string | The URL associated with an Enterprise Client. |
| `external_key` | string | External Key for the Directory. |
| `id` | string | Unique identifier for the Directory. |
| `message` | string | WorkOS response field message. |
| `metadata` | object | Aggregate counts of directory users and groups synced from the provider. |
| `name` | string | The name of the directory. |
| `object` | string | Distinguishes the Directory object. |
| `organization_id` | string | The unique identifier for the Organization in which the directory resides. |
| `state` | string | Describes whether the Directory has been successfully connected to an external provider. |
| `type` | string | The type of external Directory Provider integrated with. |
| `updated_at` | date | An ISO 8601 timestamp. |

## Native endpoint

Through the native WorkOS API, this operation is `GET /directories/{id}` (base URL `https://api.workos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-directory.md) for the provider-specific parameters and requirements.

