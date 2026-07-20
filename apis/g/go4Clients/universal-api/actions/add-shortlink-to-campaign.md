# Go4Clients: Add Shortlink to Campaign

Adds shortlinks to an existing Go4Clients campaign.

```
PUT https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-shortlink-to-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-shortlink-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shortlinkCampaignId": "69dd271fcc9a80000773ba02",
  "key[]": "mindcloud-key-1,mindcloud-key-2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-shortlink-to-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shortlinkCampaignId": "69dd271fcc9a80000773ba02",
    "key[]": "mindcloud-key-1,mindcloud-key-2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shortlinkCampaignId` | string | yes | Shortlink campaign identifier. Example: `69dd271fcc9a80000773ba02`. |
| `key[]` | array<string> | yes | List of shortlink keys to create. Example: `mindcloud-key-1,mindcloud-key-2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shortlinksApi": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shortlinksApi` | array<object> | Shortlinks created for the campaign. |

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/campaigns/shortlink/v1.0/{{shortlink_campaign_id}}` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-shortlink-to-campaign.md) for the provider-specific parameters and requirements.

