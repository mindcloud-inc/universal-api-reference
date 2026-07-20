# Fourthwall: List Collections

Retrieves a paginated list of collections from Fourthwall.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-collections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-collections?${params}`, {
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
| `search` | string | no | Search collections by keyword. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "shopId": "string",
      "slug": "string",
      "state": {
        "available": true,
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `shopId` | string |  |
| `slug` | string |  |
| `state.available` | boolean |  |
| `state.type` | string |  |

## Native endpoint

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/collections` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.

