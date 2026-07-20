# Go4Clients: Create Email Campaign

Creates a new email campaign in Go4Clients.

```
POST https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-email-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Spring promo",
  "fromName": "MindCloud Marketing",
  "fromEmail": "campaigns@example.com",
  "replyEmail": "support@example.com",
  "subject": "Your April update",
  "template": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create-email-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Spring promo",
    "fromName": "MindCloud Marketing",
    "fromEmail": "campaigns@example.com",
    "replyEmail": "support@example.com",
    "subject": "Your April update",
    "template": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name set to the campaign. Example: `Spring promo`. |
| `fromName` | string | yes | From name associated to the campaign sender email. Example: `MindCloud Marketing`. |
| `fromEmail` | string | yes | From email of the campaign. Example: `campaigns@example.com`. |
| `replyEmail` | string | yes | Email address recipients reply to. Example: `support@example.com`. |
| `subject` | string | yes | Subject used on the email campaign. Example: `Your April update`. |
| `template` | object | yes | Template object used on the campaign, for example {"body":"<html>...</html>"}. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "starDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Rendered HTML body used for the campaign. |
| `creationDate` | date | Campaign creation timestamp. |
| `id` | string | Unique email campaign identifier. |
| `name` | string | Campaign name. |
| `starDate` | date | Campaign start timestamp returned by Go4Clients. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/email/v1.0/` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-campaign.md) for the provider-specific parameters and requirements.

