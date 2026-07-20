# Moorcheh: Delete Vectors

Deletes vectors from a Moorcheh namespace by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-vectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-vectors?connectionId=$CONNECTION_ID&namespace_name=Ava%20Chen&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace_name": "Ava Chen",
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-vectors?${params}`, {
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
| `namespace_name` | string | yes | Name of the vector namespace containing vectors to delete. |
| `ids[]` | array<string> | yes | Array of vector IDs to permanently delete. Moorcheh allows up to 1000 IDs per request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual_deletions": 1,
      "message": "string",
      "remaining_items": 1,
      "requested_deletions": 1,
      "requested_ids": [
        "string"
      ],
      "status": "string",
      "unprocessed_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual_deletions` | number | Number of IDs actually deleted. |
| `message` | string | Human-readable deletion message. |
| `remaining_items` | number | Items remaining in the namespace. |
| `requested_deletions` | number | Number of IDs requested for deletion. |
| `requested_ids` | array<string> | IDs requested for deletion. |
| `status` | string | Deletion status. |
| `unprocessed_ids` | array<string> | IDs not processed in partial responses. |

## Native endpoint

Through the native Moorcheh API, this operation is `POST /namespaces/:namespace_name/vectors/delete` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-vectors.md) for the provider-specific parameters and requirements.

