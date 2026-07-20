# WEBLUCY: Search Contact by Email

Finds contacts in WEBLUCY by email address.

```
GET https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/search-contact-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/search-contact-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/search-contact-by-email?${params}`, {
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
| `email` | string | yes | The contact email address to search for. |

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

Through the native WEBLUCY API, this operation is `GET /contacts/search-by-email` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contact-by-email.md) for the provider-specific parameters and requirements.

