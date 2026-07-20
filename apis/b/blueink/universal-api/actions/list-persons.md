# Blueink: List Persons

Retrieves persons from your Blueink account.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-persons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-persons?${params}`, {
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
| `search` | string | no | Search by name, email, or phone. |
| `email` | string | no | Filter persons by email address. |
| `phone` | string | no | Filter persons by phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        {
          "email": "ava@example.com",
          "id": "string",
          "kind": "string",
          "phone": "string"
        }
      ],
      "id": "string",
      "isUser": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels[].email` | string |  |
| `channels[].id` | string |  |
| `channels[].kind` | string |  |
| `channels[].phone` | string |  |
| `id` | string |  |
| `isUser` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /persons/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-persons.md) for the provider-specific parameters and requirements.

