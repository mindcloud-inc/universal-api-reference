# Xano: Get Branch

Retrieves a branch from Xano by label.

```
GET https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-branch?connectionId=$CONNECTION_ID&branch_label=string&workspace_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "branch_label": "string",
  "workspace_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-branch?${params}`, {
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
| `branch_label` | string | yes |  |
| `workspace_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backup": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "label": "string",
      "live": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backup` | boolean |  |
| `createdAt` | date |  |
| `id` | number |  |
| `label` | string |  |
| `live` | boolean |  |

## Native endpoint

Through the native Xano API, this operation is `GET /api%3Ameta/workspace/:workspace_id/branch/:branch_label` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-branch.md) for the provider-specific parameters and requirements.

