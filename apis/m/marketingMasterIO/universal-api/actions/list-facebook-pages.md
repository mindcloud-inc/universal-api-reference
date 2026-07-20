# Marketing Master IO: List Facebook Pages

Retrieves imported Facebook pages from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-facebook-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-facebook-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-facebook-pages?${params}`, {
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
| `enabled` | string | no | Set to 1 for enabled pages or 0 for disabled pages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "enabled": true,
      "facebook_user": "string",
      "id": "string",
      "page_id": "string",
      "page_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string |  |
| `enabled` | boolean |  |
| `facebook_user` | string |  |
| `id` | string |  |
| `page_id` | string |  |
| `page_name` | string |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `GET /v1/facebook_pages` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-facebook-pages.md) for the provider-specific parameters and requirements.

