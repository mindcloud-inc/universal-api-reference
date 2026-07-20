# SMSGlobal: Get Contact

Retrieves a contact from SMSGlobal by ID.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | The contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "emailAddress": "ava@example.com",
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "groupId": "string",
      "id": 1,
      "msisdn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Display name for the contact. |
| `emailAddress` | string | Contact email address. |
| `familyName` | string | Contact family name. |
| `givenName` | string | Contact given name. |
| `groupId` | string | Owning group identifier. |
| `id` | number | Contact identifier. |
| `msisdn` | string | Contact phone number. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/contact/:id` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

