# SendPulse: Update Scheduled Campaign

Updates a scheduled campaign in SendPulse.

```
PUT https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-scheduled-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-scheduled-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "987654"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-scheduled-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "987654"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The SendPulse campaign identifier. Example: `987654`. |
| `name` | string | no | Updated campaign name. Example: `Updated March Newsletter`. |
| `subject` | string | no | Updated email subject line. Example: `Updated March Product Update`. |
| `senderName` | string | no | Updated sender display name. Example: `MindCloud Team`. |
| `senderEmail` | string | no | Updated sender email address. Example: `updates@example.com`. |
| `body` | string | no | Updated base64-encoded HTML body for the campaign. Example: `PGgxPkVkaXRlZCBDYW1wYWlnbjwvaDE+`. |
| `mailingListId` | string | no | Updated mailing list for the campaign. Example: `123456`. |
| `templateId` | string | no | Updated template identifier. Example: `345678`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendDate` | string | no | Scheduled send date and time. Example: `2026-03-20 10:00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Updated SendPulse campaign identifier. |
| `result` | boolean | Whether the scheduled campaign update request succeeded. |

## Native endpoint

Through the native SendPulse API, this operation is `PATCH /campaigns/:campaignId` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scheduled-campaign.md) for the provider-specific parameters and requirements.

