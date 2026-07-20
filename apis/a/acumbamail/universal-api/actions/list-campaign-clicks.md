# Acumbamail: List Campaign Clicks

Retrieves campaign click activity from Acumbamail.

```
GET https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/list-campaign-clicks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumbamail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/list-campaign-clicks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumbamail/latest/actions/list-campaign-clicks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumbamail API returns.

## Native endpoint

Through the native Acumbamail API, this operation is `POST /getCampaignClicks/` (base URL `https://acumbamail.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-clicks.md) for the provider-specific parameters and requirements.

