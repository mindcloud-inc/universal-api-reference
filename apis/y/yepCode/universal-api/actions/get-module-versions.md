# YepCode: Get module versions

Retrieves module version records from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module-versions?connectionId=$CONNECTION_ID&limit=25&offset=0&moduleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "moduleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module-versions?${params}`, {
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
| `moduleId` | string | yes | Unique identifier of the module whose versions you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "programmingLanguage": "string",
      "sourceCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | Comment for the module version |
| `createdAt` | date | Timestamp when the version was created |
| `createdBy` | string | Username of the user who created the version |
| `id` | string | Version identifier of the module |
| `programmingLanguage` | string | Programming language used by the module version |
| `sourceCode` | string | Source code for the module version |
| `updatedAt` | date | Timestamp when the version was last updated |
| `updatedBy` | string | Username of the user who last updated the version |

## Native endpoint

Through the native YepCode API, this operation is `GET /modules/:moduleId/versions` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-module-versions.md) for the provider-specific parameters and requirements.

