# Maildrip: Restore draft email to drafts



```
PUT https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/restore-draft-email-to-drafts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/restore-draft-email-to-drafts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "emailId": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/restore-draft-email-to-drafts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "emailId": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of the campaign |
| `emailId` | string | yes | ID of the draft email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "restoredEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `restoredEmail` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `PATCH /api/v1/campaigns/{campaignId}/{emailId}/restore-mail-to-draft` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-draft-email-to-drafts.md) for the provider-specific parameters and requirements.

