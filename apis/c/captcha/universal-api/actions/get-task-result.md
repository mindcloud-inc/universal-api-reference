# 2Captcha: Get Task Result

Retrieves the current result for a 2Captcha task.

```
GET https://connect.mindcloud.co/v1/universal/captcha/latest/actions/get-task-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Captcha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captcha/latest/actions/get-task-result?connectionId=$CONNECTION_ID&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captcha/latest/actions/get-task-result?${params}`, {
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
| `taskId` | number | yes | 2Captcha task id returned by createTask. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": "string",
      "createTime": 1,
      "endTime": 1,
      "errorId": 1,
      "ip": "string",
      "solution": {},
      "solveCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | string |  |
| `createTime` | number |  |
| `endTime` | number |  |
| `errorId` | number |  |
| `ip` | string |  |
| `solution` | object |  |
| `solveCount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native 2Captcha API, this operation is `POST /getTaskResult` (base URL `https://api.2captcha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-result.md) for the provider-specific parameters and requirements.

