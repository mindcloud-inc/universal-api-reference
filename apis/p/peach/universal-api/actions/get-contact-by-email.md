# Peach: Get Contact By Email

Retrieves a contact from Peach by email address.

```
GET https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-contact-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-contact-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peach/latest/actions/get-contact-by-email?${params}`, {
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
| `email` | string | yes | The email address to look up. |

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

Through the native Peach API, this operation is `POST /getContact` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-email.md) for the provider-specific parameters and requirements.

