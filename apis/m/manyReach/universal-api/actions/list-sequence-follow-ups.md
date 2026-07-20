# ManyReach: List Sequence Follow-Ups

Retrieves follow-ups for a sequence from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-sequence-follow-ups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-sequence-follow-ups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-sequence-follow-ups?${params}`, {
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
| `id` | string | no | Sequence ID. |

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

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/sequences/:id/followups` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sequence-follow-ups.md) for the provider-specific parameters and requirements.

