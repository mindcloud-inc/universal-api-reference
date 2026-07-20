# LaGrowthMachine: Remove Lead from Audiences

Removes a lead from audiences in LaGrowthMachine.

```
PUT https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/remove-lead-from-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaGrowthMachine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/remove-lead-from-audiences" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audience[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/remove-lead-from-audiences', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audience[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audience[]` | array<string> | yes | Audience names to remove from the lead, or use `all` to remove the lead from every audience. |
| `companyName` | string | no | Lead company name. |
| `companyUrl` | string | no | Lead company URL. |
| `crmId` | string | no | Lead CRM ID. |
| `firstname` | string | no | Lead first name. |
| `lastname` | string | no | Lead last name. |
| `linkedinUrl` | string | no | Lead LinkedIn URL. |
| `persoEmail` | string | no | Lead personal email. |
| `proEmail` | string | no | Lead professional email. |
| `twitter` | string | no | Lead Twitter profile URL or handle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `statusCode` | number | Provider status code returned after removing the lead from the selected audiences. |

## Native endpoint

Through the native LaGrowthMachine API, this operation is `POST /leads/removefromaudience` (base URL `https://apiv2.lagrowthmachine.com/flow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-lead-from-audiences.md) for the provider-specific parameters and requirements.

