# Common Ninja: Get Submission

Retrieves a project submission from Common Ninja.

```
GET https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-submission?connectionId=$CONNECTION_ID&projectId=string&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/get-submission?${params}`, {
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
| `projectId` | string | yes | The project ID. |
| `submissionId` | string | yes | The submission ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "data": [
        {}
      ],
      "projectId": "string",
      "submissionId": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "widgetId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `data` | array<object> |  |
| `projectId` | string |  |
| `submissionId` | string |  |
| `type` | string |  |
| `updated` | date |  |
| `widgetId` | string |  |

## Native endpoint

Through the native Common Ninja API, this operation is `GET /projects/:projectId/submissions/:submissionId` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission.md) for the provider-specific parameters and requirements.

