# Fliqr AI: Find Contacts By Custom Field



```
GET https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/find-contacts-by-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/find-contacts-by-custom-field?connectionId=$CONNECTION_ID&fieldId=string&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldId": "string",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/find-contacts-by-custom-field?${params}`, {
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
| `fieldId` | string | yes | Custom field ID. Use phone or email to search those built-in fields. |
| `value` | string | yes | Custom field value to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "channel": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "pageId": "string",
      "phone": "string",
      "subscribed": true,
      "tags": [
        {
          "id": "string"
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
| `accountId` | string |  |
| `channel` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `pageId` | string |  |
| `phone` | string |  |
| `subscribed` | boolean |  |
| `tags[].id` | string |  |

## Native endpoint

Through the native Fliqr AI API, this operation is `GET /users/find_by_custom_field` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-contacts-by-custom-field.md) for the provider-specific parameters and requirements.

