# DitLead: Remove Contact From List



```
PUT https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/remove-contact-from-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/remove-contact-from-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/remove-contact-from-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Public ID of the contact. |
| `listId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "message": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `POST /v1/contact/{contactId}/remove-from-list` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-from-list.md) for the provider-specific parameters and requirements.

