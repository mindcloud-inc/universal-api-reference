# Codemagic: List Tester Group Contacts

Retrieves contacts for a specific Codemagic tester group.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-tester-group-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-tester-group-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&testerGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "testerGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/list-tester-group-contacts?${params}`, {
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
| `testerGroupId` | string | yes | Codemagic tester group identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
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
| `confirmed_at` | date |  |
| `created_at` | date |  |
| `email` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/tester-groups/:tester_group_id/contacts` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tester-group-contacts.md) for the provider-specific parameters and requirements.

