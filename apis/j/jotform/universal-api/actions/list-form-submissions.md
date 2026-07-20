# Jotform: List Form Submissions

Retrieves submissions for a Jotform form.

```
GET https://connect.mindcloud.co/v1/universal/jotform/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&id=123456789012345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "123456789012345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/list-form-submissions?${params}`, {
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
| `id` | string | yes | Jotform form ID. Example: `123456789012345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "form_id": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `form_id` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Jotform API, this operation is `GET /form/:id/submissions` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

