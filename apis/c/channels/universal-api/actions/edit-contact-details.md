# Channels: Edit Contact Details

Updates existing contact details in Channels.

```
PUT https://connect.mindcloud.co/v1/universal/channels/latest/actions/edit-contact-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channels/latest/actions/edit-contact-details" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "details": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/edit-contact-details', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "details": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Contact ID whose details should be edited. |
| `details` | object | yes | Contact details object to replace or edit. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Channels API returns.

## Native endpoint

Through the native Channels API, this operation is `PUT /api/v1/contacts/{contactId}/details` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-contact-details.md) for the provider-specific parameters and requirements.

