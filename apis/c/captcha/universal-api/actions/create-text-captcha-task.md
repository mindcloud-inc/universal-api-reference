# 2Captcha: Create Text Captcha Task

Creates a text captcha task in 2Captcha.

```
POST https://connect.mindcloud.co/v1/universal/captcha/latest/actions/create-text-captcha-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Captcha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/captcha/latest/actions/create-text-captcha-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "task.comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/captcha/latest/actions/create-text-captcha-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "task.comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task.comment` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorId": 1,
      "taskId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorId` | number | 2Captcha error id. 0 means success. |
| `taskId` | number | Created 2Captcha task id. |

## Native endpoint

Through the native 2Captcha API, this operation is `POST /createTask` (base URL `https://api.2captcha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-captcha-task.md) for the provider-specific parameters and requirements.

