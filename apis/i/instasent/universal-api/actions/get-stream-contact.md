# Instasent: Get Stream Contact



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-stream-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-stream-contact?connectionId=$CONNECTION_ID&project=string&datasource=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "datasource": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-stream-contact?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `datasource` | string | yes | Datasource identifier. |
| `userId` | string | yes | Audience user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "audienceId": "string",
        "contactData": {
          "_country_code": "string",
          "_email": "ava@example.com",
          "_first_name": "Ava",
          "_last_name": "Chen",
          "_phone_mobile": "string",
          "_user_id": "string"
        },
        "contactId": "string",
        "createdAt": "string",
        "customTag": {},
        "datasourceSequence": 1,
        "deleted": true,
        "hasErrors": {},
        "id": "string",
        "temporaryContactId": {},
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.audienceId` | string |  |
| `contact.contactData._country_code` | string |  |
| `contact.contactData._email` | string |  |
| `contact.contactData._first_name` | string |  |
| `contact.contactData._last_name` | string |  |
| `contact.contactData._phone_mobile` | string |  |
| `contact.contactData._user_id` | string |  |
| `contact.contactId` | string |  |
| `contact.createdAt` | string |  |
| `contact.customTag` | object |  |
| `contact.datasourceSequence` | number |  |
| `contact.deleted` | boolean |  |
| `contact.hasErrors` | object |  |
| `contact.id` | string |  |
| `contact.temporaryContactId` | object |  |
| `contact.updatedAt` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/datasource/:datasource/stream/contacts/:userId` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stream-contact.md) for the provider-specific parameters and requirements.

