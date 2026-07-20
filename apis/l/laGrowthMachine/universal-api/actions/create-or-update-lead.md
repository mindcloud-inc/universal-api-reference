# LaGrowthMachine: Create or Update Lead

Creates or updates a lead in LaGrowthMachine.

```
PUT https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-or-update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-or-update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audience": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/create-or-update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audience": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audience` | string | yes | Audience name. |
| `bio` | string | no | Lead bio. |
| `companyName` | string | no | Lead company name. |
| `companyUrl` | string | no | Lead company URL. |
| `crmId` | string | no | Lead CRM ID. |
| `customAttribute1` | string | no | Lead custom attribute 1. |
| `customAttribute10` | string | no | Lead custom attribute 10. |
| `customAttribute2` | string | no | Lead custom attribute 2. |
| `customAttribute3` | string | no | Lead custom attribute 3. |
| `customAttribute4` | string | no | Lead custom attribute 4. |
| `customAttribute5` | string | no | Lead custom attribute 5. |
| `customAttribute6` | string | no | Lead custom attribute 6. |
| `customAttribute7` | string | no | Lead custom attribute 7. |
| `customAttribute8` | string | no | Lead custom attribute 8. |
| `customAttribute9` | string | no | Lead custom attribute 9. |
| `excludeContactedLeads` | boolean | no | Exclude leads who have already been contacted. |
| `firstname` | string | no | Lead first name. |
| `gender` | string | no | Lead gender. Accepted values are `man` or `woman`. |
| `industry` | string | no | Lead industry. |
| `jobTitle` | string | no | Lead job title. |
| `lastname` | string | no | Lead last name. |
| `leadId` | string | no | Existing lead ID to update. |
| `linkedinUrl` | string | no | Lead LinkedIn URL. |
| `location` | string | no | Lead location. |
| `persoEmail` | string | no | Lead personal email. |
| `phone` | string | no | Lead phone number. |
| `proEmail` | string | no | Lead professional email. |
| `profilePicture` | string | no | Lead profile picture URL. |
| `twitter` | string | no | Lead Twitter profile URL or handle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leadId": "string",
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leadId` | string | Identifier of the created or updated lead. |
| `message` | string | Provider message describing the lead update outcome. |
| `statusCode` | number | Provider status code returned after the lead create or update request. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `POST /leads` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-lead.md) for the provider-specific parameters and requirements.

