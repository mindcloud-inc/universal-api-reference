# ManyReach: Create Sequence Follow-Up

Creates a follow-up for a sequence in ManyReach.

```
POST https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-sequence-follow-up
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-sequence-follow-up" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "waitMin": "string",
  "waitUnits": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-sequence-follow-up', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "waitMin": "string",
    "waitUnits": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Sequence ID. |
| `waitMin` | string | yes | Wait duration amount before the follow-up. |
| `waitUnits` | string | yes | Units for the wait duration. |

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

Through the native ManyReach API, this operation is `POST https://api.manyreach.com/api/v2/sequences/:id/followups` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sequence-follow-up.md) for the provider-specific parameters and requirements.

