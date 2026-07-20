# Merit: Get Recurring Invoice Details



```
GET https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-recurring-invoice-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-recurring-invoice-details?connectionId=$CONNECTION_ID&id=2757a822-be01-4564-530d-08de9fd83d73" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2757a822-be01-4564-530d-08de9fd83d73"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/merit/latest/actions/get-recurring-invoice-details?${params}`, {
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
| `id` | string | yes | Recurring invoice ID. Example: `2757a822-be01-4564-530d-08de9fd83d73`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merit API returns.

## Native endpoint

Through the native Merit API, this operation is `POST v2/getperinvoice` (base URL `https://aktiva.merit.ee/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recurring-invoice-details.md) for the provider-specific parameters and requirements.

