# Snapchat Ads: Get Billing Center

Retrieves a billing center from Snapchat Ads.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-billing-center
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-billing-center?connectionId=$CONNECTION_ID&billingCenterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "billingCenterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-billing-center?${params}`, {
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
| `billingCenterId` | string | yes | The Snapchat Billing Center ID to retrieve. |

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

Through the native Snapchat Ads API, this operation is `GET /billingcenters/:billingCenterId` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-center.md) for the provider-specific parameters and requirements.

