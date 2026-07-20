# ActiveCampaign: Update Deal

Updates an existing deal in ActiveCampaign.

```
PUT https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The deal ID. |
| `deal` | object | no |  |
| `deal.title` | string | no |  |
| `deal.description` | string | no |  |
| `deal.account` | string | no |  |
| `deal.contact` | string | no |  |
| `deal.value` | number | no |  |
| `deal.currency` | string | no |  |
| `deal.group` | string | no |  |
| `deal.stage` | string | no |  |
| `deal.owner` | string | no |  |
| `deal.percent` | number | no |  |
| `deal.status` | number | no |  |
| `deal.fields[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCampaign API returns.

## Native endpoint

Through the native ActiveCampaign API, this operation is `PUT /deals/:id` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

