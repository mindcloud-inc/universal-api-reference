# ActiveCampaign: Create Deal

Creates a new deal in ActiveCampaign.

```
POST https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deal": {},
  "deal.title": "string",
  "deal.account": "string",
  "deal.contact": "string",
  "deal.value": 1,
  "deal.currency": "string",
  "deal.group": "string",
  "deal.stage": "string",
  "deal.owner": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deal": {},
    "deal.title": "string",
    "deal.account": "string",
    "deal.contact": "string",
    "deal.value": 1,
    "deal.currency": "string",
    "deal.group": "string",
    "deal.stage": "string",
    "deal.owner": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deal` | object | yes |  |
| `deal.title` | string | yes |  |
| `deal.description` | string | no |  |
| `deal.account` | string | yes |  |
| `deal.contact` | string | yes |  |
| `deal.value` | number | yes |  |
| `deal.currency` | string | yes |  |
| `deal.group` | string | yes |  |
| `deal.stage` | string | yes |  |
| `deal.owner` | string | yes |  |
| `deal.percent` | number | no |  |
| `deal.status` | number | no |  |
| `deal.fields[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveCampaign API returns.

## Native endpoint

Through the native ActiveCampaign API, this operation is `POST /deals` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

