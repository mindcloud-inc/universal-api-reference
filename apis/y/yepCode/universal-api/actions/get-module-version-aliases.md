# YepCode: Get module version aliases

Retrieves module version aliases from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module-version-aliases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module-version-aliases?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module-version-aliases?${params}`, {
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
| `moduleId` | string | yes | Module ID whose version aliases you want to retrieve. |
| `versionId` | string | no | Optionally filter aliases to a specific module version. |

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

Through the native YepCode API, this operation is `GET /modules/:moduleId/aliases` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-module-version-aliases.md) for the provider-specific parameters and requirements.

