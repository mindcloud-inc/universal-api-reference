# HelloLeads: Create Lead



```
POST https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelloLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "first_name": "Ava",
  "list_key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "first_name": "Ava",
    "list_key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address_line1` | string | no | First line of the lead address. |
| `address_line2` | string | no | Second line of the lead address. |
| `category` | string | no | Lead category. |
| `city` | string | no | Lead city. |
| `company` | string | no | Company or organization name. |
| `country` | string | no | Lead country. |
| `deal_size` | string | no | Lead deal size as accepted by HelloLeads. |
| `designation` | string | no | Lead designation or job title. |
| `fax` | string | no | Lead fax number. |
| `first_name` | string | yes | Lead first name. HelloLeads requires this field for lead creation. |
| `interests` | string | no | Lead interests. |
| `mobile_code` | string | no | Mobile country code prefix, for example +1. |
| `notes` | string | no | Lead notes. |
| `phone` | string | no | Lead phone number. |
| `postal_code` | string | no | Lead postal or ZIP code. |
| `potential` | string | no | Lead potential value, for example Low, Medium, or High. |
| `state` | string | no | Lead state or region. |
| `tags` | string | no | Comma-separated or provider-native tag value. |
| `website` | string | no | Lead website URL. |
| `list_key` | list | yes | HelloLeads list identifier for the destination list. Live verification used the Website Enquires list. |
| `email` | string | no | Lead email address. |
| `mobile` | string | no | Lead mobile number. |
| `last_name` | string | no | Lead last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": {},
      "lead_id": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | object | Additional provider metadata returned with the create response. |
| `lead_id` | number | Identifier of the newly created HelloLeads lead. |
| `message` | string | Provider message for the create request. |
| `status` | string | Provider status string for the create request. |

## Native endpoint

Through the native HelloLeads API, this operation is `POST leads` (base URL `https://app.helloleads.io/index.php/private/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

