# Survalyzer: Invite Members



```
POST https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/invite-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Survalyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/invite-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "panelId": 1,
  "messageTemplateId": 1,
  "channel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/invite-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "panelId": 1,
    "messageTemplateId": 1,
    "channel": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes |  |
| `panelId` | number | yes |  |
| `samplingProjectId` | number | no |  |
| `messageTemplateId` | number | yes |  |
| `textBlocks[]` | array<object> | no |  |
| `scheduleDateTime` | string | no |  |
| `conditions[]` | array<object> | no |  |
| `channel` | string | yes |  |
| `asyncProcess` | boolean | no |  |
| `interviewExpiryDate` | string | no |  |
| `from` | string | no |  |
| `fromName` | string | no |  |
| `replyTo` | string | no |  |
| `replyToName` | string | no |  |
| `memberIds[]` | array<number> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "distributorId": 1,
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "samplingProjectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `distributorId` | number | Distributor identifier returned for the invite batch. |
| `errorCode` | string |  |
| `errorMessage` | string |  |
| `isSuccess` | boolean |  |
| `samplingProjectId` | number | Sampling project created or used during the invite operation. |

## Native endpoint

Through the native Survalyzer API, this operation is `POST /publicapi/Distribute/v3/InviteMembers` (base URL `https://api.survalyzer-eu.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-members.md) for the provider-specific parameters and requirements.

