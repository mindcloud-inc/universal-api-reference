# Vouchery.io: Create Campaign



```
POST https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "name": "Ava Chen",
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "name": "Ava Chen",
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Campaign type. Use MainCampaign or SubCampaign. |
| `name` | string | yes | Campaign name. |
| `currency` | string | yes | Campaign currency code. |
| `status` | string | no | Campaign status. |
| `description` | string | no | Campaign description. |
| `team` | string | no | Campaign team. |
| `template` | string | no | Campaign template. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchery.io API returns.

## Native endpoint

Through the native Vouchery.io API, this operation is `POST /campaigns` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

