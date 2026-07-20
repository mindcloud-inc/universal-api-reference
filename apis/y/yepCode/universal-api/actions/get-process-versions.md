# YepCode: Get process versions

Retrieves process version records from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process-versions?connectionId=$CONNECTION_ID&limit=25&offset=0&processId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "processId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-process-versions?${params}`, {
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
| `processId` | string | yes | Unique identifier of the process whose versions you want to retrieve. |

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
      "parametersSchema": {
        "type": "string"
      },
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
| `comment` | string | Comment for the process version |
| `createdAt` | date | Timestamp when the version was created |
| `createdBy` | string | Username of the user who created the version |
| `id` | string | Version identifier of the process |
| `parametersSchema.type` | string | Top-level JSON Schema type for process input parameters |
| `programmingLanguage` | string | Programming language used by the process version |
| `sourceCode` | string | Source code for the process version |
| `updatedAt` | date | Timestamp when the version was last updated |
| `updatedBy` | string | Username of the user who last updated the version |

## Native endpoint

Through the native YepCode API, this operation is `GET /processes/:processId/versions` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-process-versions.md) for the provider-specific parameters and requirements.

