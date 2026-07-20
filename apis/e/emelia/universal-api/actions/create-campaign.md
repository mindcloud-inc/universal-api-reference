# Emelia: Create Campaign

Creates a new campaign in Emelia.

```
POST https://connect.mindcloud.co/v1/universal/emelia/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emelia/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Campaign name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createCampaign": {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "estimatedEnd": {},
          "lastRefreshed": {},
          "name": "Ava Chen",
          "plannedStart": {},
          "provider": {},
          "startAt": {},
          "status": "string",
          "useManyProviders": {}
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createCampaign.createdAt` | date |  |
| `data.createCampaign.estimatedEnd` | object |  |
| `data.createCampaign.lastRefreshed` | object |  |
| `data.createCampaign.name` | string |  |
| `data.createCampaign.plannedStart` | object |  |
| `data.createCampaign.provider` | object |  |
| `data.createCampaign.startAt` | object |  |
| `data.createCampaign.status` | string |  |
| `data.createCampaign.useManyProviders` | object |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

