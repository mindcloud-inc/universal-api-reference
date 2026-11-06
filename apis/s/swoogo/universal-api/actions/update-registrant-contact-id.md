# Swoogo: Update Registrant Contact ID



```
PUT https://connect.mindcloud.co/v1/universal/swoogo/latest/actions/update-registrant-contact-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swoogo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swoogo/latest/actions/update-registrant-contact-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "registrantId": 1,
  "zohoContactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swoogo/latest/actions/update-registrant-contact-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "registrantId": 1,
    "zohoContactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `registrantId` | number | yes | Swoogo registrant ID. |
| `zohoContactId` | string | yes | Zoho Contact record ID written to the hidden Swoogo field c_9721034. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Swoogo API returns.

## Native endpoint

Through the native Swoogo API, this operation is `PUT /registrants/update/:registrant_id` (base URL `https://api.swoogo.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-registrant-contact-id.md) for the provider-specific parameters and requirements.

