# Sendblue: Get Contact

Retrieves a contact from Sendblue by phone number.

```
GET https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-contact?connectionId=$CONNECTION_ID&phoneNumber=%2B14155550123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "+14155550123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/get-contact?${params}`, {
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
| `phoneNumber` | string | yes | Phone number in E.164 format. Example: `+14155550123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "companyName": "Ava Chen",
        "createdAt": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "phone": "string",
        "sendblueNumber": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.companyName` | string |  |
| `contact.createdAt` | string |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.phone` | string |  |
| `contact.sendblueNumber` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `GET /api/v2/contacts/:phone_number` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

