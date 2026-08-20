# MarketTime: List Items by Item ID



```
GET https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/list-items-by-item-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MarketTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/list-items-by-item-id?connectionId=$CONNECTION_ID&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketTime/latest/actions/list-items-by-item-id?${params}`, {
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
| `itemId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MarketTime API returns.

## Native endpoint

Through the native MarketTime API, this operation is `GET /mtpublic/api/v1/:whoAmI/items/:itemID` (base URL `https://publicapi.markettime.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-items-by-item-id.md) for the provider-specific parameters and requirements.

