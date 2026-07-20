# Intercom: Archive Contact



```
PUT https://connect.mindcloud.co/v1/universal/intercom/latest/actions/archive-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intercom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intercom/latest/actions/archive-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intercom/latest/actions/archive-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Intercom contact identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "externalId": "string",
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `externalId` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Intercom API, this operation is `POST /contacts/:contact_id/archive` (base URL `https://api.intercom.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-contact.md) for the provider-specific parameters and requirements.

