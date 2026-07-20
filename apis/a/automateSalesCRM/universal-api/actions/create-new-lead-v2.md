# Automate Sales CRM: Create New Lead V2

Creates a new lead in Automate Sales CRM.

```
POST https://connect.mindcloud.co/v1/universal/automateSalesCRM/latest/actions/create-new-lead-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Automate Sales CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/automateSalesCRM/latest/actions/create-new-lead-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/automateSalesCRM/latest/actions/create-new-lead-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Lead or contact name sent to the public lead webhook. Example: `Jane Doe`. |
| `email` | string | no | Lead email address. Example: `jane@example.com`. |
| `phone` | string | no | Lead phone number. Example: `+15551234567`. |
| `leadTitle` | string | no | Lead title from the provider's lead-creation UI. Example: `Website Inquiry`. |
| `source` | string | no | Lead source label. Example: `MindCloud`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pipeline` | string | no | Optional pipeline label when workspace defaults are not sufficient. Example: `Default`. |
| `stage` | string | no | Optional stage label when workspace defaults are not sufficient. Example: `New`. |
| `salesPerson` | string | no | Optional sales person or assignee label from the provider UI. Example: `Default Sales Rep`. |

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
| `message` | string | Raw provider response text from the public lead webhook. |

## Native endpoint

Through the native Automate Sales CRM API, this operation is `POST ab-crm-webhook` (base URL `https://api.automatebusiness.com/functions/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-lead-v2.md) for the provider-specific parameters and requirements.

