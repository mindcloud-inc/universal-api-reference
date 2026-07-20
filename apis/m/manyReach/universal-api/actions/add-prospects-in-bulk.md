# ManyReach: Add Prospects in Bulk

Creates prospects in bulk in ManyReach.

```
POST https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/add-prospects-in-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/add-prospects-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "prospects": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/add-prospects-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "prospects": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Required list ID to which all prospects will be added |
| `campaignId` | string | no | Optional campaign ID to add prospects to |
| `addOnlyIfNew` | boolean | no | Only add prospects that are new in CRM |
| `notInOtherCampaign` | boolean | no | Check if prospect is already in other campaigns |
| `prospects` | list<object> | yes | Array of prospect objects to create in bulk. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignAdded": 1,
      "duplicatesInBatch": 1,
      "prospectsInserted": 1,
      "prospectsUpdated": 1,
      "subscriptionsAdded": 1,
      "totalProcessed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignAdded` | number |  |
| `duplicatesInBatch` | number |  |
| `prospectsInserted` | number |  |
| `prospectsUpdated` | number |  |
| `subscriptionsAdded` | number |  |
| `totalProcessed` | number |  |

## Native endpoint

Through the native ManyReach API, this operation is `POST https://api.manyreach.com/api/v2/prospects/bulk` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-prospects-in-bulk.md) for the provider-specific parameters and requirements.

