# YepCode: Get process version alias

Retrieves a process version alias from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process-version-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process-version-alias?connectionId=$CONNECTION_ID&processId=string&aliasId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "processId": "string",
  "aliasId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process-version-alias?${params}`, {
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
| `processId` | string | yes | Process ID whose alias you want to retrieve. |
| `aliasId` | string | yes | Alias ID to retrieve. |

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
| `createdAt` | date | Timestamp when the alias was created |
| `createdBy` | string | Username of the user who created the alias |
| `id` | string | Alias identifier |
| `name` | string | Alias name |
| `updatedAt` | date | Timestamp when the alias was last updated |
| `updatedBy` | string | Username of the user who last updated the alias |
| `versionId` | string | Version ID currently assigned to the alias |

## Native endpoint

Through the native YepCode API, this operation is `GET /processes/:processId/aliases/:aliasId` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-process-version-alias.md) for the provider-specific parameters and requirements.

