# respond.io: Merge Contacts

Merges two contacts in respond.io.

```
PUT https://connect.mindcloud.co/v1/universal/respondio/latest/actions/merge-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/merge-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactIds": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/respondio/latest/actions/merge-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactIds": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactIds` | object | yes | IDs of the two contacts to merge. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |

## Native endpoint

Through the native respond.io API, this operation is `POST /contact/merge` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-contacts.md) for the provider-specific parameters and requirements.

