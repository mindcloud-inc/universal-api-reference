# Wiza: Get List

Retrieves a Wiza list by ID.

```
GET https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-list?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-list?${params}`, {
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
| `id` | number | yes | ID of the list to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "enrichment_level": "string",
        "finished_at": "string",
        "id": 1,
        "name": "Ava Chen",
        "stats": {
          "people": 1
        },
        "status": "string"
      },
      "status": {
        "code": 1,
        "message": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.enrichment_level` | string | Requested enrichment level. |
| `data.finished_at` | string | Completion timestamp when available. |
| `data.id` | number | List ID. |
| `data.name` | string | List name. |
| `data.stats.people` | number | Number of people in the list. |
| `data.status` | string | Current list status. |
| `status.code` | number | HTTP-style status code returned by Wiza. |
| `status.message` | string | Status message from Wiza. |
| `type` | string | Response type identifier. |

## Native endpoint

Through the native Wiza API, this operation is `GET /lists/:id` (base URL `https://wiza.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

