# Merit: Get Purchase Invoice Details



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-purchase-invoice-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-purchase-invoice-details?connectionId=$CONNECTION_ID&id=79e76261-a3ac-4a48-b624-08de9fd84182" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "79e76261-a3ac-4a48-b624-08de9fd84182"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-purchase-invoice-details?${params}`, {
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
| `id` | string | yes | Purchase invoice ID. Example: `79e76261-a3ac-4a48-b624-08de9fd84182`. |
| `fillAccCodes` | boolean | no | Whether to fill account code details when supported. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merit API returns.

## Native endpoint

Through the native Merit API, this operation is `POST v2/getpurchorder` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-invoice-details.md) for the provider-specific parameters and requirements.

