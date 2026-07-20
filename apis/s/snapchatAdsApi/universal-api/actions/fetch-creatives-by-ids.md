# Snapchat Ads: Fetch Creatives by IDs

Retrieves creatives from Snapchat Ads by creative IDs.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-creatives-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-creatives-by-ids?connectionId=$CONNECTION_ID&adAccountId=string&creativeIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string",
  "creativeIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-creatives-by-ids?${params}`, {
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
| `adAccountId` | string | yes | The Snapchat Ad Account ID that owns the creatives. |
| `creativeIds` | list<string> | yes | An array of Snapchat Creative IDs to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creatives": [
        {
          "creative": {
            "id": "string",
            "name": "Ava Chen",
            "status": "string",
            "type": "string"
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
| `creatives[].creative.id` | string |  |
| `creatives[].creative.name` | string |  |
| `creatives[].creative.status` | string |  |
| `creatives[].creative.type` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `POST /adaccounts/:adAccountId/get_creatives_by_ids` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-creatives-by-ids.md) for the provider-specific parameters and requirements.

