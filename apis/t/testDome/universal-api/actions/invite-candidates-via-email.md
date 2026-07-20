# TestDome: Invite Candidates Via Email

Invites candidates via email in TestDome.

```
POST https://connect.mindcloud.co/v1/universal/testDome/latest/actions/invite-candidates-via-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/invite-candidates-via-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deadline": "string",
  "emailBody": "ava@example.com",
  "emails": "ava@example.com",
  "proctoringEnabled": true,
  "replyTo": "string",
  "testId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/invite-candidates-via-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deadline": "string",
    "emailBody": "ava@example.com",
    "emails": "ava@example.com",
    "proctoringEnabled": true,
    "replyTo": "string",
    "testId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deadline` | string | yes |  |
| `emailBody` | string | yes |  |
| `emails` | list<string> | yes |  |
| `proctoringEnabled` | boolean | yes |  |
| `replyTo` | string | yes |  |
| `testId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "failedEmails": [
        "ava@example.com"
      ],
      "message": "string",
      "result": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Dictionary |
| `failedEmails` | array<string> | The emails of the invitations that failed to be sent. |
| `message` | string | The message that describes an error, if any, in the invitation request. If everything worked as expected, this will be `null`. |
| `result` | array<string> | The results of the invitation request. |

## Native endpoint

Through the native TestDome API, this operation is `POST /tests/:testId/candidates/invite-via-email` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-candidates-via-email.md) for the provider-specific parameters and requirements.

