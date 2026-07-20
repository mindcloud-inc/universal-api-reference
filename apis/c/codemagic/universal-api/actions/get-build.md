# Codemagic: Get Build

Retrieves a specific build from Codemagic.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build?connectionId=$CONNECTION_ID&buildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "buildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build?${params}`, {
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
      "app_id": "string",
      "artifacts": [
        {}
      ],
      "branch": "string",
      "build_inputs": {},
      "commit": {},
      "config": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "finished_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "index": 1,
      "labels": [
        "string"
      ],
      "release_notes": [
        {}
      ],
      "remote_access_enabled": true,
      "started_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tag": "string",
      "workflow": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_id` | string |  |
| `artifacts` | array<object> |  |
| `branch` | string |  |
| `build_inputs` | object |  |
| `commit` | object |  |
| `config` | object |  |
| `created_at` | date |  |
| `finished_at` | date |  |
| `id` | string |  |
| `index` | number |  |
| `labels` | array<string> |  |
| `release_notes` | array<object> |  |
| `remote_access_enabled` | boolean |  |
| `started_at` | date |  |
| `status` | string |  |
| `tag` | string |  |
| `workflow` | object |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/builds/:build_id` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-build.md) for the provider-specific parameters and requirements.

