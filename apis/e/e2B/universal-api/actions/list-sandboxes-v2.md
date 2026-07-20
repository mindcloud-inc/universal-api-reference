# E2B: List Sandboxes V2

Retrieves a list of sandboxes from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes-v2?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes-v2?${params}`, {
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
| `metadata` | string | no | Optional URL-encoded metadata query used to filter sandboxes. |
| `state` | string | no | Filter sandboxes by one or more states. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "endAt": "2026-05-07T12:00:00.000Z",
      "envdVersion": "string",
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
| `endAt` | date | Time when the sandbox will expire. |
| `envdVersion` | string | Version of envd running in the sandbox. |
| `metadata` | object | Sandbox metadata. |
| `sandboxID` | string | Identifier of the sandbox. |
| `startedAt` | date | Time when the sandbox was started. |
| `state` | string | Sandbox state. |
| `templateID` | string | Identifier of the template from which the sandbox was created. |
| `volumeMounts` | array<object> | Mounted volumes. |

## Native endpoint

Through the native E2B API, this operation is `GET /v2/sandboxes` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sandboxes-v2.md) for the provider-specific parameters and requirements.

