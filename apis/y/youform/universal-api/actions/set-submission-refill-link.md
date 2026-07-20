# Youform: Set Submission Refill Link

Enables or disables a submission refill link in Youform.

```
PUT https://connect.mindcloud.co/v1/universal/youform/latest/actions/set-submission-refill-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Youform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/youform/latest/actions/set-submission-refill-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "submissionId": 1,
  "enable": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youform/latest/actions/set-submission-refill-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "submissionId": 1,
    "enable": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `submissionId` | number | yes | Numeric ID of the submission whose refill link you want to enable or disable. |
| `enable` | boolean | yes | Set to true to enable the refill link or false to disable it. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Youform API returns.

## Native endpoint

Through the native Youform API, this operation is `POST /submissions/:submissionId/refill-link` (base URL `https://app.youform.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-submission-refill-link.md) for the provider-specific parameters and requirements.

