# TxtSync: Add Campaign Connection

Adds recipients to a campaign in TxtSync.

```
POST https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/add-campaign-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TxtSync `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/add-campaign-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/txtSync/latest/actions/add-campaign-connection', {
  method: 'POST',
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
| `id` | number | yes |  |
| `contactIds` | list<number> | no | Accepts multiple values as an array. |
| `tagIds` | list<number> | no | Accepts multiple values as an array. |
| `numbers` | list<string> | no | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CampaignConnectionID": 1,
      "CampaignID": 1,
      "ContactID": 1,
      "ContactName": "Ava Chen",
      "CustomerID": 1,
      "TagID": 1,
      "TagName": "Ava Chen",
      "ToNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CampaignConnectionID` | number |  |
| `CampaignID` | number |  |
| `ContactID` | number |  |
| `ContactName` | string |  |
| `CustomerID` | number |  |
| `TagID` | number |  |
| `TagName` | string |  |
| `ToNumber` | string |  |

## Native endpoint

Through the native TxtSync API, this operation is `POST /campaigns/:id/connections` (base URL `https://api.txtsync.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-campaign-connection.md) for the provider-specific parameters and requirements.

