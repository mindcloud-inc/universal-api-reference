# Quo: Get Contact By ID

Retrieves a contact from Quo by ID.

```
GET https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-contact-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quo/latest/actions/get-contact-by-id?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "createdByUserId": "string",
      "defaultFields": {
        "company": "string",
        "emails": [
          {
            "id": "ava@example.com",
            "name": "ava@example.com",
            "value": "ava@example.com"
          }
        ],
        "firstName": "Ava",
        "lastName": "Chen",
        "phoneNumbers": [
          {
            "id": "string",
            "name": "Ava Chen",
            "value": "string"
          }
        ],
        "role": "string"
      },
      "externalId": {},
      "id": "string",
      "source": {},
      "sourceUrl": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `createdByUserId` | string |  |
| `defaultFields.company` | string |  |
| `defaultFields.emails[].id` | string |  |
| `defaultFields.emails[].name` | string |  |
| `defaultFields.emails[].value` | string |  |
| `defaultFields.firstName` | string |  |
| `defaultFields.lastName` | string |  |
| `defaultFields.phoneNumbers[].id` | string |  |
| `defaultFields.phoneNumbers[].name` | string |  |
| `defaultFields.phoneNumbers[].value` | string |  |
| `defaultFields.role` | string |  |
| `externalId` | object |  |
| `id` | string |  |
| `source` | object |  |
| `sourceUrl` | object |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Quo API, this operation is `GET /contacts/:id` (base URL `https://api.openphone.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-id.md) for the provider-specific parameters and requirements.

