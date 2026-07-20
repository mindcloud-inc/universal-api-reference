# Foreplay: Get Spyder Brand

Retrieves a tracked Spyder brand from Foreplay.

```
GET https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-spyder-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foreplay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-spyder-brand?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-spyder-brand?${params}`, {
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
| `brandId` | string | no | The brand ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ad_library_id": "string",
      "avatar": "string",
      "category": "string",
      "description": {
        "text": "string"
      },
      "id": "string",
      "is_delegate_page_with_linked_primary_profile": true,
      "name": "Ava Chen",
      "url": "https://example.com",
      "verification_status": "string",
      "websites": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ad_library_id` | string |  |
| `avatar` | string |  |
| `category` | string |  |
| `description.text` | string |  |
| `id` | string |  |
| `is_delegate_page_with_linked_primary_profile` | boolean |  |
| `name` | string |  |
| `url` | string |  |
| `verification_status` | string |  |
| `websites[]` | string |  |

## Native endpoint

Through the native Foreplay API, this operation is `GET /api/spyder/brand` (base URL `https://public.api.foreplay.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spyder-brand.md) for the provider-specific parameters and requirements.

