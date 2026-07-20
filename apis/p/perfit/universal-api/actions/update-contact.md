# Perfit: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/perfit/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perfit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/perfit/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perfit/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "contactId": "string"
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
| `firstName` | string | no | Updated first name. |
| `lastName` | string | no | Updated last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        {}
      ],
      "firstName": "Ava",
      "id": 1,
      "lastModified": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array<object> |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastModified` | date |  |
| `lastName` | string |  |

## Native endpoint

Through the native Perfit API, this operation is `PUT /:account/contacts/:contactId` (base URL `https://api.myperfit.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

