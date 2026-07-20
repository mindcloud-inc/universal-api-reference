# Brevo: Create Email Campaign



```
POST https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-email-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "htmlContent": "string",
  "name": "Ava Chen",
  "recipients": {},
  "sender": {},
  "subject": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-email-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "htmlContent": "string",
    "name": "Ava Chen",
    "recipients": {},
    "sender": {},
    "subject": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `htmlContent` | string | yes | HTML content of the email. |
| `name` | string | yes | Email campaign name. |
| `recipients` | object | yes | Recipients object containing list IDs or segment IDs. |
| `sender` | object | yes | Sender object with name and email. |
| `subject` | string | yes | Email campaign subject line. |
| `type` | string | no | Campaign type, for example classic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/emailCampaigns` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-campaign.md) for the provider-specific parameters and requirements.

