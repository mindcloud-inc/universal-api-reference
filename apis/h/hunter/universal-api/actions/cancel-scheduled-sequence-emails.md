# Hunter: Cancel Scheduled Sequence Emails



```
PUT https://connect.mindcloud.co/v1/universal/hunter/latest/actions/cancel-scheduled-sequence-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/cancel-scheduled-sequence-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hunter/latest/actions/cancel-scheduled-sequence-emails', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "emails": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Identifier of the sequence. |
| `emails` | list<string> | yes | Email addresses whose scheduled messages should be canceled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messagesCanceled": 1,
      "recipientsCanceled": [
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
| `messagesCanceled` | number |  |
| `recipientsCanceled` | array<string> |  |

## Native endpoint

Through the native Hunter API, this operation is `DELETE /campaigns/:campaignId/recipients` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-scheduled-sequence-emails.md) for the provider-specific parameters and requirements.

