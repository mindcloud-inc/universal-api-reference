# Payrexx: Update Pre-Authorization Tokenization Contact Details

Updates pre-authorization or tokenization contact details in Payrexx.

```
PUT https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/update-pre-authorization-tokenization-contact-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/update-pre-authorization-tokenization-contact-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123456",
  "fields": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/update-pre-authorization-tokenization-contact-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123456",
    "fields": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the Pre-Authorization / Tokenization. Example: `123456`. |
| `fields` | object | yes | The contact data fields which should be stored. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `PUT Transaction/:id/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pre-authorization-tokenization-contact-details.md) for the provider-specific parameters and requirements.

