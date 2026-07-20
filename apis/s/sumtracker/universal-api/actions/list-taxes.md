# Sumtracker: List Taxes

Retrieves tax rates from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-taxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-taxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-taxes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sumtracker API returns.

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/settings/taxes/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-taxes.md) for the provider-specific parameters and requirements.

