# Eventee: List Registrations

Retrieves registrations from Eventee.

```
GET https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-registrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-registrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-registrations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "bio": "string",
      "company": "string",
      "email": "ava@example.com",
      "emailValid": true,
      "facebookLink": "https://example.com",
      "firstName": "Ava",
      "groupId": 1,
      "id": 1,
      "lastName": "Chen",
      "linkedInLink": "https://example.com",
      "phone": "string",
      "photo": "string",
      "position": "string",
      "sendEmail": true,
      "status": "string",
      "twitterLink": "https://example.com",
      "web": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bio` | string | Registrant biography. |
| `company` | string | Registrant company. |
| `email` | string | Registrant email. |
| `emailValid` | boolean | Whether the email address is valid. |
| `facebookLink` | string | Registrant Facebook URL. |
| `firstName` | string | Registrant first name. |
| `groupId` | number | Assigned group ID. |
| `id` | number | Registration ID. |
| `lastName` | string | Registrant last name. |
| `linkedInLink` | string | Registrant LinkedIn URL. |
| `phone` | string | Registrant phone number. |
| `photo` | string | Registrant photo URL. |
| `position` | string | Registrant position title. |
| `sendEmail` | boolean | Whether invite email should be sent. |
| `status` | string | Registration status code. |
| `twitterLink` | string | Registrant Twitter URL. |
| `web` | string | Registrant website URL. |

## Native endpoint

Through the native Eventee API, this operation is `GET /registrations` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-registrations.md) for the provider-specific parameters and requirements.

