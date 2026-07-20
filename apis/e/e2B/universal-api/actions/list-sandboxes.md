# E2B: List Sandboxes

Retrieves a list of running sandboxes from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes?${params}`, {
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
| `metadata` | string | no | Optional URL-encoded metadata query used to filter sandboxes, such as user=abc&app=prod. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "clientID": "string",
      "cpuCount": 1,
      "diskSizeMB": 1,
      "endAt": "2026-05-07T12:00:00.000Z",
      "envdVersion": "string",
      "memoryMB": 1,
      "metadata": {},
      "sandboxID": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "templateID": "string",
      "volumeMounts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Template alias. |
| `clientID` | string | Deprecated client identifier. |
| `cpuCount` | number | CPU cores for the sandbox. |
| `diskSizeMB` | number | Disk size for the sandbox in MiB. |
| `endAt` | date | Time when the sandbox will expire. |
| `envdVersion` | string | Version of envd running in the sandbox. |
| `memoryMB` | number | Memory for the sandbox in MiB. |
| `metadata` | object | Sandbox metadata. |
| `sandboxID` | string | Identifier of the sandbox. |
| `startedAt` | date | Time when the sandbox was started. |
| `state` | string | Sandbox state. |
| `templateID` | string | Identifier of the template from which the sandbox was created. |
| `volumeMounts` | array<object> | Mounted volumes. |

## Native endpoint

Through the native E2B API, this operation is `GET /sandboxes` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sandboxes.md) for the provider-specific parameters and requirements.

