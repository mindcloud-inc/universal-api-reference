# Perfit: Add Interest To Contact



```
PUT https://connect.mindcloud.co/v1/universal/perfit/latest/actions/add-interest-to-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perfit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/add-interest-to-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "contactId": "string",
  "interest": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perfit/latest/actions/add-interest-to-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "contactId": "string",
    "interest": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | string | yes | Perfit account name. |
| `contactId` | string | yes | Contact email or numeric ID. |
| `interest` | string | yes | Existing Perfit interest ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "subscribed": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `subscribed` | date |  |

## Native endpoint

Through the native Perfit API, this operation is `PUT /:account/contacts/:contactId/interests/:interest` (base URL `https://api.myperfit.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-interest-to-contact.md) for the provider-specific parameters and requirements.

