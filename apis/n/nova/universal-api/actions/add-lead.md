# Nova: Add Lead



```
POST https://connect.mindcloud.co/v1/universal/nova/latest/actions/add-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nova/latest/actions/add-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_id": "28",
  "phone_number_concatenated": "+33777777777"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nova/latest/actions/add-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_id": "28",
    "phone_number_concatenated": "+33777777777"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_id` | number | yes | Target Nova live list identifier. Default: `28`. Example: `28`. |
| `phone_number_concatenated` | string | yes | Lead phone number. Nova docs also allow an array, but this action currently models the common single-number case. Default: `+33777777777`. Example: `+33777777777`. |
| `firstname` | string | no | Lead first name. Example: `John`. |
| `lastname` | string | no | Lead last name. Example: `Doe`. |
| `email` | string | no | Lead email address. Example: `john.doe@example.com`. |
| `origin_crm_id` | string | no | External lead identifier in your CRM. Example: `crm-123`. |
| `statut` | string | no | Nova lead status label. Example: `Sans statut`. |
| `assigned_to` | string | no | Nova user ID assigned to the lead. Example: `10537`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_id": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "lastname": "Chen",
      "list_id": 1,
      "phone_number_concatenated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_id` | string | Nova access token for opening the created lead debug view. |
| `email` | string | Lead email address. |
| `firstname` | string | Lead first name. |
| `lastname` | string | Lead last name. |
| `list_id` | number | Nova list identifier where the lead was created. |
| `phone_number_concatenated` | string | Lead phone number stored in Nova. |

## Native endpoint

Through the native Nova API, this operation is `POST /rt/zapier/add/lead` (base URL `https://app.n0va.com/v1/la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-lead.md) for the provider-specific parameters and requirements.

