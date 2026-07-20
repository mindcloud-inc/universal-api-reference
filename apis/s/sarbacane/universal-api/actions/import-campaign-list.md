# Sarbacane: Import Campaign List

Imports a list into a campaign in Sarbacane.

```
POST https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/import-campaign-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/import-campaign-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/import-campaign-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | no | Sarbacane campaign ID. |
| `listId` | string | no | Sarbacane list ID to import into the campaign. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sarbacane API returns.

## Native endpoint

Through the native Sarbacane API, this operation is `POST /campaigns/{campaignId}/list` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-campaign-list.md) for the provider-specific parameters and requirements.

