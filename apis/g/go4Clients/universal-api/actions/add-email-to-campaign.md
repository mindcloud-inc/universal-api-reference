# Go4Clients: Add Email to Campaign

Adds email recipients to an existing Go4Clients campaign.

```
PUT https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-email-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-email-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "69dd2653841fc80008eba9e1",
  "destinationsList[]": "apps@mindcloud.co",
  "landingCustomFields": "[object Object]",
  "fromEmail": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-email-to-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "69dd2653841fc80008eba9e1",
    "destinationsList[]": "apps@mindcloud.co",
    "landingCustomFields": "[object Object]",
    "fromEmail": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Email campaign identifier. Example: `69dd2653841fc80008eba9e1`. |
| `destinationsList[]` | array<string> | yes | Email destination list. Example: `apps@mindcloud.co`. |
| `landingCustomFields` | object | yes | Map of custom fields keyed by destination email. Example: `[object Object]`. |
| `fromEmail` | string | yes | From email used in the email sent. Example: `apps@mindcloud.co`. |
| `fromName` | string | no | From name associated to the sender email. Example: `Apps MindCloud`. |
| `subject` | string | no | Subject of the email. Example: `MindCloud follow-up email`. |
| `priority` | string | no | Priority of the email. Example: `LOW`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "destinationsList": [
        "string"
      ],
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "generatedIds": {},
      "landingCustomFields": {},
      "priority": "string",
      "replyEmail": "ava@example.com",
      "subject": "string",
      "waitForAddOn": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string | Identifier of the email campaign. |
| `destinationsList` | array<string> | Destinations included in the request. |
| `fromEmail` | string | From email used for the message. |
| `fromName` | string | From name used for the message. |
| `generatedIds` | object | Generated IDs mapped to destinations. |
| `landingCustomFields` | object | Custom fields keyed by destination. |
| `priority` | string | Priority of the message. |
| `replyEmail` | string | Reply-to email used for the message. |
| `subject` | string | Subject of the message. |
| `waitForAddOn` | number | Wait time before add-on processing. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/email/v1.0/{{campaignId}}` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-email-to-campaign.md) for the provider-specific parameters and requirements.

