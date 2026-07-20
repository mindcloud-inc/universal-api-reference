# gyfti: Add Contact to Email Campaign

Adds a contact to an email campaign in gyfti.

```
POST https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-contact-to-email-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a gyfti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-contact-to-email-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign": "string",
  "contactEmail": "ava@example.com",
  "contactFirstname": "Ava",
  "contactLastname": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gyfti/latest/actions/add-contact-to-email-campaign', {
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
    "contactLastname": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign` | string | yes | The gyfti trigger campaign ID to add the contact to. |
| `contactEmail` | string | yes | Recipient email address. |
| `contactFirstname` | string | yes | Recipient first name. |
| `contactLastname` | string | yes | Recipient last name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | Recipient company name. |
| `jobtitle` | string | no | Recipient job title. |
| `phone` | string | no | Recipient phone number. |
| `address` | string | no | Recipient street address. |
| `additionalAddress` | string | no | Recipient additional address details. |
| `postalCode` | string | no | Recipient postal code. |
| `city` | string | no | Recipient city. |
| `country` | string | no | Recipient country. |

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

Through the native gyfti API, this operation is `POST /wf/1_zapier_add_contact_trigger/` (base URL `https://app.gyfti.fr/api/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-email-campaign.md) for the provider-specific parameters and requirements.

