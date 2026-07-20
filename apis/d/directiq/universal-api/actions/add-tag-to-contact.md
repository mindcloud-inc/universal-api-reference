# DirectIQ: Add Tag to Contact

Adds a tag to a contact in DirectIQ.

```
PUT https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-tag-to-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-tag-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-tag-to-contact', {
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

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "id": 1,
      "tagId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |
| `id` | number |  |
| `tagId` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `POST /contacts/tag/assign` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tag-to-contact.md) for the provider-specific parameters and requirements.

