# LinkedCamp: Add Leads To Campaign



```
POST https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/add-leads-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedCamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/add-leads-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "leads[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/add-leads-to-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "leads[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | Campaign identifier. |
| `leads[]` | array<object> | yes | Array of leads to add to the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | LinkedCamp status message. |
| `success` | boolean | Whether the operation succeeded. |

## Native endpoint

Through the native LinkedCamp API, this operation is `POST /leads/add-to-campaign` (base URL `https://api.linkedcamp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-leads-to-campaign.md) for the provider-specific parameters and requirements.

