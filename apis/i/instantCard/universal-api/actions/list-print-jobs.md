# InstantCard: List Print Jobs

Retrieves a list of print jobs from InstantCard.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-print-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-print-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=20003827" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "20003827"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-print-jobs?${params}`, {
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
| `organizationId` | number | yes | Organization ID from your InstantCard account. Example: `20003827`. |
| `status` | number | no | Optional print job status filter: 0 for created jobs or 1 for submitted jobs. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "address_id": 1,
      "created_at": "string",
      "extract": {},
      "id": 1,
      "list_users": [
        {}
      ],
      "organization": {},
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address_id` | number |  |
| `created_at` | string |  |
| `extract` | object |  |
| `id` | number |  |
| `list_users` | array<object> |  |
| `organization` | object |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/print_jobs` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-print-jobs.md) for the provider-specific parameters and requirements.

