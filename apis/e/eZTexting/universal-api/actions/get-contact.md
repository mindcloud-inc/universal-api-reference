# EZ Texting: Get Contact

Retrieves a contact from EZ Texting by phone number.

```
GET https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZ Texting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-contact?connectionId=$CONNECTION_ID&phoneNumber=(737)%20337-8315" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "(737) 337-8315"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZTexting/latest/actions/get-contact?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNumber` | string | yes | Phone number Example: `(737) 337-8315`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "custom1": "string",
      "custom2": "string",
      "custom3": "string",
      "custom4": "string",
      "custom5": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "groups": [
        [
          {}
        ]
      ],
      "lastName": "Chen",
      "note": "string",
      "optOut": true,
      "phoneNumber": "string",
      "source": "string",
      "values": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `custom1` | string |  |
| `custom2` | string |  |
| `custom3` | string |  |
| `custom4` | string |  |
| `custom5` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `groups[]` | array<object> |  |
| `groups[].contactsCount` | number |  |
| `groups[].id` | string |  |
| `groups[].name` | string |  |
| `groups[].note` | string |  |
| `lastName` | string |  |
| `note` | string |  |
| `optOut` | boolean |  |
| `phoneNumber` | string |  |
| `source` | string |  |
| `values` | object |  |

## Native endpoint

Through the native EZ Texting API, this operation is `GET /contacts/:phoneNumber` (base URL `https://a.eztexting.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

