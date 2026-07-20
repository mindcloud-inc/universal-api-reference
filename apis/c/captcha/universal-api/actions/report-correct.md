# 2Captcha: Report Correct

Marks a 2Captcha task result as correct.

```
PUT https://connect.mindcloud.co/v1/universal/captcha/latest/actions/report-correct
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Captcha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/captcha/latest/actions/report-correct" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/captcha/latest/actions/report-correct', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | number | yes | Task id to report as correctly solved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native 2Captcha API, this operation is `POST /reportCorrect` (base URL `https://api.2captcha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-correct.md) for the provider-specific parameters and requirements.

