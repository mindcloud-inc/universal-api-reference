# Agility CMS: Get Content Item V1 (Fetch)

Retrieves a published content item from Agility CMS v1.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-content-item-v1-fetch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-content-item-v1-fetch?connectionId=$CONNECTION_ID&id=112" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "112"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-content-item-v1-fetch?${params}`, {
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
| `id` | number | yes | The contentID of the item to retrieve. Example: `112`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentID": 1,
      "fields": {},
      "properties": {},
      "seo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentID` | number |  |
| `fields` | object |  |
| `properties` | object |  |
| `seo` | object |  |

## Native endpoint

Through the native Agility CMS API, this operation is `GET /v1/:guid/fetch/:locale/item/:id` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-item-v1-fetch.md) for the provider-specific parameters and requirements.

