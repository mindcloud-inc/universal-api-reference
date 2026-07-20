# Jodoo: Get Workflow Instance Logs



```
GET https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-workflow-instance-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-workflow-instance-logs?connectionId=$CONNECTION_ID&instanceId=659cba93489a49c06f7d4281&types%5B%5D=comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "instanceId": "659cba93489a49c06f7d4281",
  "types[]": "comment"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-workflow-instance-logs?${params}`, {
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
| `instanceId` | string | yes | Workflow instance ID, which is the same value as the workflow record data ID. Example: `659cba93489a49c06f7d4281`. |
| `types[]` | array<string> | yes | Array of workflow log types to return, such as `comment` or `operate`. Example: `comment`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of logs to skip before returning results. Example: `0`. |
| `limit` | number | no | Maximum number of logs to return. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
        {
          "attachments": [
            {
              "mime": "string",
              "name": "Ava Chen",
              "size": 1,
              "url": "https://example.com"
            }
          ],
          "comment": "string",
          "createAction": "string",
          "createTime": "2026-05-07T12:00:00.000Z",
          "finishAction": "string",
          "finishTime": "2026-05-07T12:00:00.000Z",
          "flowId": 1,
          "flowName": "Ava Chen",
          "operator": {
            "departments": [
              1
            ],
            "name": "Ava Chen",
            "status": 1,
            "type": 1,
            "username": "Ava Chen"
          },
          "signature": {
            "url": "https://example.com"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logs[].attachments[].mime` | string |  |
| `logs[].attachments[].name` | string |  |
| `logs[].attachments[].size` | number |  |
| `logs[].attachments[].url` | string |  |
| `logs[].comment` | string |  |
| `logs[].createAction` | string |  |
| `logs[].createTime` | date |  |
| `logs[].finishAction` | string |  |
| `logs[].finishTime` | date |  |
| `logs[].flowId` | number |  |
| `logs[].flowName` | string |  |
| `logs[].operator.departments[]` | number |  |
| `logs[].operator.name` | string |  |
| `logs[].operator.status` | number |  |
| `logs[].operator.type` | number |  |
| `logs[].operator.username` | string |  |
| `logs[].signature.url` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST https://api.jodoo.com/api/v1/workflow/instance/logs` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow-instance-logs.md) for the provider-specific parameters and requirements.

