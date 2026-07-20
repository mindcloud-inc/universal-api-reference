# Brevo: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-contact?${params}`, {
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
| `identifier` | string | yes | Contact identifier (email or contact ID). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "sms": "string"
      },
      "createdAt": "string",
      "email": "ava@example.com",
      "emailBlacklisted": true,
      "id": 1,
      "listIds": [
        1
      ],
      "modifiedAt": "string",
      "smsBlacklisted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.sms` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `emailBlacklisted` | boolean |  |
| `id` | number |  |
| `listIds[]` | number |  |
| `modifiedAt` | string |  |
| `smsBlacklisted` | boolean |  |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/contacts/:identifier` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

