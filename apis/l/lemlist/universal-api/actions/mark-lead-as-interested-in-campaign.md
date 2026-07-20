# lemlist: Mark Lead as Interested in Campaign

Marks a lead as interested in a lemlist campaign.

```
PUT https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/mark-lead-as-interested-in-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/mark-lead-as-interested-in-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "campaign_123",
  "leadIdOrEmail": "jane.doe@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/mark-lead-as-interested-in-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "campaign_123",
    "leadIdOrEmail": "jane.doe@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The ID of the campaign containing the lead. Example: `campaign_123`. |
| `leadIdOrEmail` | string | yes | The lead identifier or email address. Example: `jane.doe@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "companyName": "Ava Chen",
      "contactId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isPaused": true,
      "jobTitle": "string",
      "lastName": "Chen",
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
| `companyName` | string |  |
| `contactId` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `isPaused` | boolean |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `preferredContactMethod` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `POST /campaigns/:campaignId/leads/:leadIdOrEmail/interested` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-lead-as-interested-in-campaign.md) for the provider-specific parameters and requirements.

