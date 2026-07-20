# lemlist: Create Lead in Campaign

Creates a new lead in a lemlist campaign.

```
POST https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/create-lead-in-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/create-lead-in-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "campaign_123",
  "email": "jane.doe@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/create-lead-in-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "campaign_123",
    "email": "jane.doe@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | The ID of the campaign to add the lead to. Example: `campaign_123`. |
| `email` | string | yes | The lead's email address. Example: `jane.doe@example.com`. |
| `firstName` | string | no | The lead's first name. Example: `Jane`. |
| `lastName` | string | no | The lead's last name. Example: `Doe`. |
| `companyName` | string | no | The lead's company name. Example: `Acme`. |
| `jobTitle` | string | no | The lead's job title. Example: `Growth Lead`. |
| `linkedinUrl` | string | no | The lead's LinkedIn profile URL. Example: `https://linkedin.com/in/jane-doe`. |
| `picture` | string | no | The lead's profile picture URL. Example: `https://example.com/avatar.jpg`. |
| `phone` | string | no | The lead's phone number. Example: `+15555550123`. |
| `companyDomain` | string | no | The lead's company domain. Example: `example.com`. |
| `icebreaker` | string | no | A custom icebreaker to personalize outreach. Example: `Congrats on the product launch`. |
| `timezone` | string | no | The lead's timezone. Example: `Europe/Paris`. |
| `contactOwner` | string | no | The lead owner's email address. Example: `owner@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deduplicate` | boolean | no | Prevents duplicate leads from being added when enabled. Example: `true`. |
| `linkedinEnrichment` | boolean | no | Enrich the lead with LinkedIn data if available. Example: `true`. |
| `findEmail` | boolean | no | Find an email address for the lead when one is not provided. Example: `true`. |
| `verifyEmail` | boolean | no | Verify the provided or found email address. Example: `true`. |
| `findPhone` | boolean | no | Find a phone number for the lead if available. Example: `true`. |

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
      "lastName": "Chen"
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
| `lastName` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `POST /campaigns/:campaignId/leads/` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead-in-campaign.md) for the provider-specific parameters and requirements.

