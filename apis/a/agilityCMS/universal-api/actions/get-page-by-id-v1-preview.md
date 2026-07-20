# Agility CMS: Get Page By ID V1 (Preview)

Retrieves a preview page by ID from Agility CMS v1.

```
GET https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-page-by-id-v1-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agility CMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-page-by-id-v1-preview?connectionId=$CONNECTION_ID&id=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-page-by-id-v1-preview?${params}`, {
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
| `id` | number | yes | The pageID of the page to retrieve. Example: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "menuText": "string",
      "name": "Ava Chen",
      "pageID": 1,
      "pageType": "string",
      "path": "string",
      "properties": {},
      "scripts": {},
      "seo": {},
      "templateName": "Ava Chen",
      "title": "string",
      "visible": {},
      "zones": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `menuText` | string |  |
| `name` | string |  |
| `pageID` | number |  |
| `pageType` | string |  |
| `path` | string |  |
| `properties` | object |  |
| `scripts` | object |  |
| `seo` | object |  |
| `templateName` | string |  |
| `title` | string |  |
| `visible` | object |  |
| `zones` | object |  |

## Native endpoint

Through the native Agility CMS API, this operation is `GET /v1/:guid/preview/:locale/page/:id` (base URL `https://api.aglty.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-by-id-v1-preview.md) for the provider-specific parameters and requirements.

