# YepCode: Create process version alias

Creates a process version alias in YepCode.

```
POST https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-process-version-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-process-version-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "processId": "string",
  "name": "Ava Chen",
  "versionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/create-process-version-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "processId": "string",
    "name": "Ava Chen",
    "versionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `processId` | string | yes |  |
| `name` | string | yes |  |
| `versionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `versionId` | string |  |

## Native endpoint

Through the native YepCode API, this operation is `POST /processes/:processId/aliases` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-process-version-alias.md) for the provider-specific parameters and requirements.

