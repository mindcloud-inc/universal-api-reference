# DirectIQ: Remove a tag from a contact using tag name and contact email

Removes a tag from a DirectIQ contact by tag name and email.

```
PUT https://connect.mindcloud.co/v1/universal/directiq/latest/actions/remove-a-tag-from-a-contact-using-tag-name-and-contact-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/remove-a-tag-from-a-contact-using-tag-name-and-contact-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directiq/latest/actions/remove-a-tag-from-a-contact-using-tag-name-and-contact-email', {
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

Through the native DirectIQ API, this operation is `PUT /contacts/tag/removecontact` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-a-tag-from-a-contact-using-tag-name-and-contact-email.md) for the provider-specific parameters and requirements.

