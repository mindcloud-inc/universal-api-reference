# Snapchat Ads: List Billing Centers

Retrieves billing centers from Snapchat Ads.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-billing-centers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-billing-centers?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/list-billing-centers?${params}`, {
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
| `organizationId` | string | yes | The Snapchat Organization ID that owns the billing centers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingcenters": [
        {
          "billingcenter": {
            "id": "string",
            "name": "Ava Chen",
            "status": "string"
          }
        }
      ],
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingcenters[].billingcenter.id` | string |  |
| `billingcenters[].billingcenter.name` | string |  |
| `billingcenters[].billingcenter.status` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `GET /organizations/:organizationId/billingcenters` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-billing-centers.md) for the provider-specific parameters and requirements.

