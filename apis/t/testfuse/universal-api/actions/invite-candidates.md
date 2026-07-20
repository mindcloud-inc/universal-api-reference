# Testfuse: Invite Candidates

Invites candidates to a Testfuse assessment spec.

```
POST https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/invite-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testfuse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/invite-candidates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ],
  "specId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testfuse/latest/actions/invite-candidates', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"],
    "specId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes |  |
| `specId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Testfuse API, this operation is `POST /v1/users/invite_multiple_candidates` (base URL `https://gateway.testfuse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-candidates.md) for the provider-specific parameters and requirements.

