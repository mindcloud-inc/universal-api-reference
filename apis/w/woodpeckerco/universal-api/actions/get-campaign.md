# Woodpecker.co: Get Campaign

Retrieves a single campaign from Woodpecker.

```
GET https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woodpecker.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | number | yes | Campaign ID from Woodpecker. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Woodpecker.co API returns.

## Native endpoint

Through the native Woodpecker.co API, this operation is `GET /rest/v2/campaigns/[:campaign_id]` (base URL `https://api.woodpecker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

