# Codemagic: Get Build Actions

Retrieves actions for a specific Codemagic build.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build-actions?connectionId=$CONNECTION_ID&limit=25&offset=0&buildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "buildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build-actions?${params}`, {
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
| `buildId` | string | yes | Codemagic build identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finished_at": "2026-05-07T12:00:00.000Z",
      "has_test_results": true,
      "id": "string",
      "name": "Ava Chen",
      "script": "string",
      "started_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finished_at` | date |  |
| `has_test_results` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `script` | string |  |
| `started_at` | date |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/builds/:build_id/actions` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-build-actions.md) for the provider-specific parameters and requirements.

