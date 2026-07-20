# DirectIQ: Add Contacts to List

Adds multiple contacts to a list in DirectIQ.

```
PUT https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-contacts-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-contacts-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directiq/latest/actions/add-contacts-to-list', {
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
      "addedToList": 1,
      "alreadyExisting": 1,
      "duplicatesInList": 1,
      "foundBounced": 1,
      "foundInSuppressionList": 1,
      "inserted": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedToList` | number |  |
| `alreadyExisting` | number |  |
| `duplicatesInList` | number |  |
| `foundBounced` | number |  |
| `foundInSuppressionList` | number |  |
| `inserted` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `POST /contacts/lists/importcontacts/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contacts-to-list.md) for the provider-specific parameters and requirements.

