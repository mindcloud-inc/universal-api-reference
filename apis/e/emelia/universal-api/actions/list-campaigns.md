# Emelia: List Campaigns

Retrieves campaign listings from Emelia.

```
GET https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-campaigns?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `options` | string | no | Filter/options JSON for the campaign list query. Provide a JSON object string, for example {"status":"running"}. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "allCampaigns": [
          {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "name": "Ava Chen",
            "plannedStart": {},
            "provider": {},
            "status": "string",
            "useManyProviders": {}
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.allCampaigns[].createdAt` | date |  |
| `data.allCampaigns[].name` | string |  |
| `data.allCampaigns[].plannedStart` | object |  |
| `data.allCampaigns[].provider` | object |  |
| `data.allCampaigns[].status` | string |  |
| `data.allCampaigns[].useManyProviders` | object |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

