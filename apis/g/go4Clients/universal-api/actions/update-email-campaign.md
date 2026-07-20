# Go4Clients: Update Email Campaign

Updates an existing email campaign in Go4Clients.

```
PUT https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-email-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "69dd2653841fc80008eba9e1",
  "name": "MindCloud API Email Campaign Updated",
  "subject": "MindCloud API update",
  "fromEmail": "apps@mindcloud.co",
  "replyEmail": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/update-email-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "69dd2653841fc80008eba9e1",
    "name": "MindCloud API Email Campaign Updated",
    "subject": "MindCloud API update",
    "fromEmail": "apps@mindcloud.co",
    "replyEmail": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Email campaign identifier. Example: `69dd2653841fc80008eba9e1`. |
| `name` | string | yes | New name of the campaign. Example: `MindCloud API Email Campaign Updated`. |
| `template` | object | no | New template body or template object used by the email. Example: `[object Object]`. |
| `description` | string | no | Optional campaign description. Example: `Updated from MindCloud`. |
| `numberOfEmail` | number | no | Sending rate quantity for the campaign. Example: `100`. |
| `minutes` | number | no | Time frame in minutes for the sending rate. Example: `15`. |
| `campaignStatus` | string | no | Campaign status value. Example: `SENT`. |
| `subject` | string | yes | Subject of the email campaign. Example: `MindCloud API update`. |
| `fromEmail` | string | yes | From email used on the campaign. Example: `apps@mindcloud.co`. |
| `replyEmail` | string | yes | Reply email for the campaign. Example: `apps@mindcloud.co`. |

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
| `body` | string | Email body content. |
| `creationDate` | date | Campaign creation date. |
| `id` | string | Identifier of the email campaign. |
| `name` | string | Name of the email campaign. |
| `starDate` | date | Campaign start date. |

## Native endpoint

Through the native Go4Clients API, this operation is `PUT /api/campaigns/email/v1.0/{{campaignId}}` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-email-campaign.md) for the provider-specific parameters and requirements.

