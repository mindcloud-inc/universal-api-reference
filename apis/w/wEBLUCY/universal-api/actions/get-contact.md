# WEBLUCY: Get Contact

Retrieves a contact from WEBLUCY.

```
GET https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | The contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "createdOn": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "note": "string",
      "phone": "string",
      "properties": [
        {}
      ],
      "state": "string",
      "subscribed": true,
      "subscriberLists": [
        1
      ],
      "tags": [
        "string"
      ],
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `createdOn` | number |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `note` | string |  |
| `phone` | string |  |
| `properties` | array<object> |  |
| `state` | string |  |
| `subscribed` | boolean |  |
| `subscriberLists` | array<number> |  |
| `tags` | array<string> |  |
| `zip` | string |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `GET /contacts/{id}` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

