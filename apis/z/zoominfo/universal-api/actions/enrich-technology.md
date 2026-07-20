# Zoominfo: Enrich Technology

Enriches technology details with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-technology
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-technology?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-technology?${params}`, {
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
| `companyId` | string | no | The id of the company for which you want to view technologies |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attribute": "string",
      "category": "string",
      "categoryParent": "string",
      "createdTime": "string",
      "description": "string",
      "domain": "string",
      "logo": "string",
      "modifiedTime": "string",
      "product": "string",
      "tag": "string",
      "vendor": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attribute` | string |  |
| `category` | string |  |
| `categoryParent` | string |  |
| `createdTime` | string |  |
| `description` | string |  |
| `domain` | string |  |
| `logo` | string |  |
| `modifiedTime` | string |  |
| `product` | string |  |
| `tag` | string |  |
| `vendor` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/tech` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-technology.md) for the provider-specific parameters and requirements.

