# ManyReach: Update Follow-Up

Updates an existing follow-up in ManyReach.

```
PUT https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-follow-up
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-follow-up" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/update-follow-up', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Followup ID. |
| `waitMin` | string | no | Updated wait duration amount. |
| `waitUnits` | string | no | Updated wait duration units. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "bounceCount": 1,
      "clickCount": 1,
      "followupId": 1,
      "interestedCount": 1,
      "openCount": 1,
      "replyCount": 1,
      "replyInThread": true,
      "replyInThreadToFollowupId": 1,
      "sendInSameThread": true,
      "sentCount": 1,
      "sequenceId": 1,
      "subject": "string",
      "useOriginalSubject": true,
      "waitMin": 1,
      "waitUnits": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `bounceCount` | number |  |
| `clickCount` | number |  |
| `followupId` | number |  |
| `interestedCount` | number |  |
| `openCount` | number |  |
| `replyCount` | number |  |
| `replyInThread` | boolean |  |
| `replyInThreadToFollowupId` | number |  |
| `sendInSameThread` | boolean |  |
| `sentCount` | number |  |
| `sequenceId` | number |  |
| `subject` | string |  |
| `useOriginalSubject` | boolean |  |
| `waitMin` | number |  |
| `waitUnits` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `PATCH https://api.manyreach.com/api/v2/followups/:id` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-follow-up.md) for the provider-specific parameters and requirements.

