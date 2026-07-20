# Marketing Master IO: Get Facebook Page

Retrieves an imported Facebook page from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-facebook-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-facebook-page?connectionId=$CONNECTION_ID&page_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/get-facebook-page?${params}`, {
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
| `page_id` | string | yes |  |

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

Through the native Marketing Master IO API, this operation is `GET /v1/facebook_pages/:page_id` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-facebook-page.md) for the provider-specific parameters and requirements.

