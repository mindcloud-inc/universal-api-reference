# CloudContactAI: Get Contact by ID



```
GET https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-contact-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-contact-by-id?${params}`, {
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
| `id` | string | no | The contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockIncomingSMS": true,
      "clientExternalId": "string",
      "clientId": 1,
      "collectionInfo": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "disabledAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "enableBotResponse": true,
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "notes": "string",
      "originalPhone": "string",
      "pending": 1,
      "phone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userClientId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockIncomingSMS` | boolean |  |
| `clientExternalId` | string |  |
| `clientId` | number |  |
| `collectionInfo` | object |  |
| `createdAt` | date |  |
| `data` | object |  |
| `disabledAt` | date |  |
| `email` | string |  |
| `enableBotResponse` | boolean |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `lists` | array<object> |  |
| `notes` | string |  |
| `originalPhone` | string |  |
| `pending` | number |  |
| `phone` | string |  |
| `updatedAt` | date |  |
| `userClientId` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `GET api/v2/contacts/:id` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-id.md) for the provider-specific parameters and requirements.

