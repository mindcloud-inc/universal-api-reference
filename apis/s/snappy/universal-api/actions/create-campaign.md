# Snappy: Create Campaign

Creates a new campaign in Snappy.

```
POST https://connect.mindcloud.co/v1/universal/snappy/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snappy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "companyId": "string",
  "customization": {},
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snappy/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "companyId": "string",
    "customization": {},
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes |  |
| `companyId` | string | yes |  |
| `customization` | object | yes |  |
| `name` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snappy API returns.

## Native endpoint

Through the native Snappy API, this operation is `POST /campaigns` (base URL `https://api.snappy.com/public-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

