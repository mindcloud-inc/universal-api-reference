# Zoominfo: Enrich Hashtags

Enriches company hashtags with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-hashtags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-hashtags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-hashtags?${params}`, {
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
| `companyId` | string | no | The id of the company for which you want to view hashtags |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categorizedFlag": true,
      "description": "string",
      "displayLabel": "string",
      "displayScore": "string",
      "group": "string",
      "hidden": true,
      "label": "string",
      "parentCategory": "string",
      "priority": 1,
      "searchString": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categorizedFlag` | boolean |  |
| `description` | string |  |
| `displayLabel` | string |  |
| `displayScore` | string |  |
| `group` | string |  |
| `hidden` | boolean |  |
| `label` | string |  |
| `parentCategory` | string |  |
| `priority` | number |  |
| `searchString` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/hashtag` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-hashtags.md) for the provider-specific parameters and requirements.

