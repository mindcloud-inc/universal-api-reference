# FogBugz: List Categories

Retrieves categories from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "fDeleted": true,
      "fIsScheduleItem": true,
      "iOrder": 1,
      "ixAttachmentIcon": 1,
      "ixCategory": 1,
      "ixStatusDefault": 1,
      "ixStatusDefaultActive": 1,
      "nIconType": 1,
      "sCategory": "string",
      "sPlural": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fDeleted` | boolean | Whether the category is deleted. |
| `fIsScheduleItem` | boolean | Whether the category is a schedule item. |
| `iOrder` | number | Display order. |
| `ixAttachmentIcon` | number | Attachment icon ID. |
| `ixCategory` | number | Category ID. |
| `ixStatusDefault` | number | Default status ID. |
| `ixStatusDefaultActive` | number | Default active status ID. |
| `nIconType` | number | Icon type code. |
| `sCategory` | string | Category name. |
| `sPlural` | string | Plural category name. |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listCategories` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

