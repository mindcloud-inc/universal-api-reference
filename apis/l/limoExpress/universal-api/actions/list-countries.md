# LimoExpress: List Countries

Retrieves countries from the LimoExpress platform.

```
GET https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-countries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-countries?${params}`, {
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
| `searchString` | string | no | Search across country fields. |
| `page` | number | no | Page number, default is 1. |
| `perPage` | number | no | Items per page, default is 20. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | ISO country code. |
| `id` | string | Country identifier. |
| `name` | string | Country display name. |

## Native endpoint

Through the native LimoExpress API, this operation is `GET /api/integration/countries` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-countries.md) for the provider-specific parameters and requirements.

