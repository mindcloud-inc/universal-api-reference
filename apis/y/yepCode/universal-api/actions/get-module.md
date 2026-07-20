# YepCode: Get module

Retrieves details for a module from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-module?${params}`, {
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
| `id` | string | yes | Unique identifier of the module to retrieve. |

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
| `createdAt` | date | Timestamp when the script library module was created |
| `createdBy` | string | Username of the user who created the module |
| `id` | string | Unique identifier (UUID) of the script library module |
| `name` | string | Name of the script library module |
| `programmingLanguage` | string | Programming language used by the module |
| `sourceCode` | string | Module source code |
| `updatedAt` | date | Timestamp when the script library module was last updated |
| `updatedBy` | string | Username of the user who last updated the module |

## Native endpoint

Through the native YepCode API, this operation is `GET /modules/:id` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-module.md) for the provider-specific parameters and requirements.

