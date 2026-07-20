# gyfti: Add Contact to Postal Campaign

Adds a contact to a postal campaign in gyfti.

```
POST https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-contact-to-postal-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gyfti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-contact-to-postal-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign": "string",
  "contactEmail": "ava@example.com",
  "contactFirstname": "Ava",
  "contactLastname": "Chen",
  "address": "string",
  "phone": "string",
  "city": "string",
  "postalCode": "string",
  "country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-contact-to-postal-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign": "string",
    "contactEmail": "ava@example.com",
    "contactFirstname": "Ava",
    "contactLastname": "Chen",
    "address": "string",
    "phone": "string",
    "city": "string",
    "postalCode": "string",
    "country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign` | string | yes | The gyfti postal trigger campaign ID to add the contact to. |
| `contactEmail` | string | yes | Recipient email address. |
| `contactFirstname` | string | yes | Recipient first name. gyfti's postal endpoint documents this external key as contact_fistname. |
| `contactLastname` | string | yes | Recipient last name. |
| `address` | string | yes | Recipient street address. |
| `phone` | string | yes | Recipient phone number. |
| `city` | string | yes | Recipient city. |
| `postalCode` | string | yes | Recipient postal code. |
| `country` | string | yes | Recipient country. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `additionalAddress` | string | no | Recipient additional address details. |
| `jobtitle` | string | no | Recipient job title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object |  |
| `status` | string |  |

## Native endpoint

Through the native gyfti API, this operation is `POST /wf/1_zapier_add_contact_trigger_directe/` (base URL `https://app.gyfti.fr/api/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-postal-campaign.md) for the provider-specific parameters and requirements.

