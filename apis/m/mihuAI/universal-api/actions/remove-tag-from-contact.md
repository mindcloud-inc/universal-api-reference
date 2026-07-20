# Mihu AI: Remove Tag from Contact



```
PUT https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/remove-tag-from-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/remove-tag-from-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/remove-tag-from-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagId` | number | no |  |
| `uuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryCode": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customField_1": "string",
      "customField_2": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "numberType": "string",
      "phoneNumber": "string",
      "preferredContactChannel": "string",
      "preferredContactTime": "string",
      "primaryLanguage": "string",
      "status": "string",
      "surname": "Ava Chen",
      "tags": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryCode` | string |  |
| `createdAt` | date |  |
| `customField_1` | string |  |
| `customField_2` | string |  |
| `email` | string |  |
| `name` | string |  |
| `numberType` | string |  |
| `phoneNumber` | string |  |
| `preferredContactChannel` | string |  |
| `preferredContactTime` | string |  |
| `primaryLanguage` | string |  |
| `status` | string |  |
| `surname` | string |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `timezone` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `POST /api/v1/contacts/:uuid/remove-tag` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag-from-contact.md) for the provider-specific parameters and requirements.

