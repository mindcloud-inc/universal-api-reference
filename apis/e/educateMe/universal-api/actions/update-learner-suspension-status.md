# EducateMe: Update Learner Suspension Status

Updates a learner's suspension status in EducateMe.

```
PUT https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-learner-suspension-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-learner-suspension-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "codex.learner.one.20260331@example.com",
  "isSuspended": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-learner-suspension-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "codex.learner.one.20260331@example.com",
    "isSuspended": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Learner email. Example: `codex.learner.one.20260331@example.com`. |
| `isSuspended` | boolean | yes | Whether the learner is suspended. Default: `true`. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the learner suspension update succeeded. |

## Native endpoint

Through the native EducateMe API, this operation is `POST /students/:email` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-learner-suspension-status.md) for the provider-specific parameters and requirements.

