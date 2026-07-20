# CoachAccountable: Delete Invoice Payment

Deletes an invoice payment from CoachAccountable.

```
DELETE https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/delete-invoice-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/delete-invoice-payment?connectionId=$CONNECTION_ID&paymentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paymentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/delete-invoice-payment?${params}`, {
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
| `paymentId` | number | yes | The ID of the Invoice Payment which is to be deleted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-invoice-payment.md) for the provider-specific parameters and requirements.

