# Facebook: Ad Campaign Query



```
GET https://connect.mindcloud.co/v1/universal/facebook/latest/actions/ad-campaign-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Facebook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/ad-campaign-query?connectionId=$CONNECTION_ID&accountID=act_1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountID": "act_1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/facebook/latest/actions/ad-campaign-query?${params}`, {
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
| `accountID` | string | yes | The Meta ad account ID, including the act_ prefix. Example: `act_1234567890`. |
| `fields` | string | no | Accepts multiple values as an array. Example: `id,account_id,name,account_status,business,balance,amount_spent`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Facebook API returns.

## Native endpoint

Through the native Facebook API, this operation is `GET /:accountID` (base URL `https://graph.facebook.com/v25.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ad-campaign-query.md) for the provider-specific parameters and requirements.

