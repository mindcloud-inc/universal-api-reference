# NetSuite - Advanced: Delete Customer Payment



```
DELETE https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/delete-customer-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Advanced `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/delete-customer-payment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/delete-customer-payment?${params}`, {
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
| `recordId` | list<string> | no | Example: `123456`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetSuite - Advanced API returns.

## Native endpoint

Through the native NetSuite - Advanced API, this operation is `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` (base URL `https://{{credentials.accountId}}.suitetalk.api.netsuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer-payment.md) for the provider-specific parameters and requirements.

