# YepCode: Get executions

Retrieves a list of executions from YepCode.

```
GET https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-executions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YepCode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-executions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yepCode/latest/actions/get-executions?${params}`, {
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
| `keywords` | string | no | Search keywords applied to process name or execution comment. |
| `processId` | string | no | Filter executions by process ID. |
| `status` | string | no | Filter executions by status. |
| `from` | date | no | Filter executions created from this date and time. |
| `to` | date | no | Filter executions created until this date and time. |
| `comment` | string | no | Filter executions by comment text. |

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
      "processId": "string",
      "returnValue": "string",
      "scheduledId": "string",
      "settings": {
        "agentPoolSlug": "string",
        "timeout": 1
      },
      "status": "string",
      "timeline": {
        "explanation": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | Optional execution comment |
| `createdAt` | date | Timestamp when the execution was started |
| `createdBy` | string | Username of the user who initiated the execution |
| `id` | string | Unique identifier (UUID) of the execution |
| `processId` | string | Unique identifier (UUID) of the process that was executed |
| `returnValue` | string | Return value from the process execution when available |
| `scheduledId` | string | Unique identifier (UUID) of the scheduled process that triggered the execution, when applicable |
| `settings.agentPoolSlug` | string | Agent pool where the execution ran |
| `settings.timeout` | number | Execution timeout in milliseconds |
| `status` | string | Current execution status |
| `timeline.explanation` | string | Explanation associated with the execution timeline |

## Native endpoint

Through the native YepCode API, this operation is `GET /executions` (base URL `https://cloud.yepcode.io/api/{{credentials.team}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-executions.md) for the provider-specific parameters and requirements.

