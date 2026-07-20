# Digiclose: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contacts?${params}`, {
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
| `exact` | string | no | Set to 1 for exact matches instead of partial matches. |
| `search` | string | no | Search contacts by name, email, phone, or company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "email": "ava@example.com",
      "fields": [
        {
          "id": 1,
          "required": true,
          "value": "string"
        }
      ],
      "formatted": "string",
      "id": 1,
      "phone": {},
      "values": {
        "city": {},
        "company": "string",
        "country": {},
        "email": "ava@example.com",
        "firstname": {},
        "lastname": {},
        "phone": {},
        "postcode": {},
        "state": {},
        "street": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `email` | string |  |
| `fields[].id` | number |  |
| `fields[].required` | boolean |  |
| `fields[].value` | string |  |
| `formatted` | string |  |
| `id` | number |  |
| `phone` | object |  |
| `values.city` | object |  |
| `values.company` | string |  |
| `values.country` | object |  |
| `values.email` | string |  |
| `values.firstname` | object |  |
| `values.lastname` | object |  |
| `values.phone` | object |  |
| `values.postcode` | object |  |
| `values.state` | object |  |
| `values.street` | object |  |

## Native endpoint

Through the native Digiclose API, this operation is `GET /contacts` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

