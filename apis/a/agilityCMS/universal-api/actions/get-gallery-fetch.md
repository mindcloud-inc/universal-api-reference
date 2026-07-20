# Agility CMS: Get Gallery (Fetch)

Retrieves a published gallery from Agility CMS.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-gallery-fetch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-gallery-fetch?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-gallery-fetch?${params}`, {
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
| `id` | number | yes | The Agility CMS gallery ID to retrieve. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "description": "string",
      "galleryId": 1,
      "media": [
        {
          "fileName": "Ava Chen",
          "mediaID": 1,
          "metaData": {},
          "modifiedOn": "string",
          "size": 1,
          "url": "https://example.com"
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `description` | string |  |
| `galleryId` | number |  |
| `media` | array<object> |  |
| `media[].fileName` | string |  |
| `media[].mediaID` | number |  |
| `media[].metaData` | object |  |
| `media[].modifiedOn` | string |  |
| `media[].size` | number |  |
| `media[].url` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Agility CMS API, this operation is `GET /v2/:guid/fetch/gallery/:id` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gallery-fetch.md) for the provider-specific parameters and requirements.

