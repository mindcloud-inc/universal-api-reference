# Diffy: Get Diff

Retrieves a single diff from Diffy.

```
GET https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-diff
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-diff?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diffy/latest/actions/get-diff?${params}`, {
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
| `id` | number | yes | Diff ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archiveUrl": "https://example.com",
      "date": "string",
      "diffSharedUrl": "https://example.com",
      "name": "Ava Chen",
      "project": {},
      "reviewed": {},
      "state": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archiveUrl` | string | Archive URL for the diff. |
| `date` | string | Diff creation date. |
| `diffSharedUrl` | string | Shared diff URL. |
| `name` | string | Diff name. |
| `project` | object | Owning project summary. |
| `reviewed` | object | Review summary. |
| `state` | number | Diff state code. |

## Native endpoint

Through the native Diffy API, this operation is `GET /diffs/:id` (base URL `https://app.diffy.website/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-diff.md) for the provider-specific parameters and requirements.

