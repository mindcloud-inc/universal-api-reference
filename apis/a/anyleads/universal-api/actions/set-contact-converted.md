# Anyleads: Set Contact Converted

Updates a contact as converted in Anyleads.

```
PUT https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/set-contact-converted
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anyleads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/set-contact-converted" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anyleads/latest/actions/set-contact-converted', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Contact email used to mark the contact as converted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Anyleads API returns.

## Native endpoint

Through the native Anyleads API, this operation is `POST /api-product/incoming-webhook/set-contact-converted` (base URL `https://myapiconnect.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-contact-converted.md) for the provider-specific parameters and requirements.

