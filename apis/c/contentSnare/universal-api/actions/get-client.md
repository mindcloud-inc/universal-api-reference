# Content Snare: Get Client

Retrieves a client from Content Snare.

```
GET https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Content Snare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-client?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/get-client?${params}`, {
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
| `id` | string | yes | Client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "client_companies": [
        {
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "company_name": "Ava Chen",
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": "string",
      "language_code": "string",
      "last_name": "Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `client_companies[].id` | string |  |
| `client_companies[].name` | string |  |
| `company_name` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `id` | string |  |
| `language_code` | string |  |
| `last_name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native Content Snare API, this operation is `GET /partner_api/v1/clients/{id}` (base URL `https://api.contentsnare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

