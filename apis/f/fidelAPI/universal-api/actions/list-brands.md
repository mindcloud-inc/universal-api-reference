# Fidel API: List Brands

Retrieves brands from Fidel API.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-brands?${params}`, {
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
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "consent": true,
      "created": "string",
      "id": "string",
      "live": true,
      "name": "Ava Chen",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `consent` | boolean |  |
| `created` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `name` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /brands` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-brands.md) for the provider-specific parameters and requirements.

