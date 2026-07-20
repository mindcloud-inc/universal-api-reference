# lemlist: Update Lead in a Campaign

Updates an existing lead in a lemlist campaign.

```
PUT https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/update-lead-in-a-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/update-lead-in-a-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "cam_123",
  "leadId": "lea_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/update-lead-in-a-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "cam_123",
    "leadId": "lea_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The ID of the campaign containing the lead. Example: `cam_123`. |
| `leadId` | string | yes | The ID of the lead to update. Example: `lea_123`. |
| `firstName` | string | no | The lead's first name. Example: `Jane`. |
| `lastName` | string | no | The lead's last name. Example: `Doe`. |
| `companyName` | string | no | The lead's company name. Example: `Example Co`. |
| `jobTitle` | string | no | The lead's job title. Example: `Head of Sales`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preferredContactMethod` | string | no | Preferred contact method for the lead. Example: `email`. |
| `contactOwner` | string | no | Owner of the contact in lemlist. Example: `usr_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "campaignName": "Ava Chen",
      "companyName": "Ava Chen",
      "contactId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isPaused": true,
      "jobTitle": "string",
      "lastName": "Chen",
      "leadUrl": "https://example.com",
      "preferredContactMethod": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string |  |
| `campaignName` | string |  |
| `companyName` | string |  |
| `contactId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isPaused` | boolean |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `leadUrl` | string |  |
| `preferredContactMethod` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `PATCH /campaigns/:campaignId/leads/:leadId` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-in-a-campaign.md) for the provider-specific parameters and requirements.

