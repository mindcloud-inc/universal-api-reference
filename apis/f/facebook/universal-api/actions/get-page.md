# Facebook: Get Page



```
GET https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Facebook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-page?connectionId=$CONNECTION_ID&pageId=102424701587913" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "102424701587913"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-page?${params}`, {
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
| `pageId` | string | yes | The Facebook Page ID. Example: `102424701587913`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Fields returned for the Page. Accepts multiple values in one string. Default: `id`. Example: `id,name,category,link,fan_count`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "fan_count": 1,
      "id": "string",
      "link": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Page category. |
| `fan_count` | number | Number of people who like the Page. |
| `id` | string | Page ID. |
| `link` | string | Public Page URL. |
| `name` | string | Page name. |

## Native endpoint

Through the native Facebook API, this operation is `GET :pageId` (base URL `https://graph.facebook.com/v25.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

