# lemlist: Pause Lead

Pauses an existing lead in lemlist.

```
PUT https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/pause-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/pause-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "lead_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/pause-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "lead_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadId` | string | yes | The ID of the lead to pause. Example: `lead_123`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | no | Pause the lead only in this specific campaign. Example: `campaign_123`. |

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

Through the native lemlist API, this operation is `POST /leads/pause/:leadId` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pause-lead.md) for the provider-specific parameters and requirements.

