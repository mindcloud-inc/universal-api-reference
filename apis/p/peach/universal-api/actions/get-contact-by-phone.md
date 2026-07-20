# Peach: Get Contact By Phone

Retrieves a contact from Peach by phone number.

```
GET https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-contact-by-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-contact-by-phone?connectionId=$CONNECTION_ID&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-contact-by-phone?${params}`, {
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
| `phoneNumber` | string | yes | The phone number to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "address": "string",
          "aptNumber": "string",
          "city": "string",
          "contactId": "string",
          "customProperties": {},
          "email": "ava@example.com",
          "firstName": "Ava",
          "groups": [
            "string"
          ],
          "lastName": "Chen",
          "street": "string",
          "streetNumber": "string",
          "telephone": "string",
          "zipCode": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> |  |
| `contacts[].address` | string |  |
| `contacts[].aptNumber` | string |  |
| `contacts[].city` | string |  |
| `contacts[].contactId` | string |  |
| `contacts[].customProperties` | object |  |
| `contacts[].email` | string |  |
| `contacts[].firstName` | string |  |
| `contacts[].groups` | array<string> |  |
| `contacts[].lastName` | string |  |
| `contacts[].street` | string |  |
| `contacts[].streetNumber` | string |  |
| `contacts[].telephone` | string |  |
| `contacts[].zipCode` | string |  |

## Native endpoint

Through the native Peach API, this operation is `POST /getContact` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-phone.md) for the provider-specific parameters and requirements.

