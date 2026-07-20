# DirectIQ: Remove a contact by email from a list

Removes a contact from a DirectIQ list by email.

```
PUT https://connect.mindcloud.co/v1/universal/directiq/latest/actions/remove-a-contact-by-email-from-a-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/remove-a-contact-by-email-from-a-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directiq/latest/actions/remove-a-contact-by-email-from-a-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DirectIQ API returns.

## Native endpoint

Through the native DirectIQ API, this operation is `PUT /contacts/lists/removecontactbyemail/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-a-contact-by-email-from-a-list.md) for the provider-specific parameters and requirements.

