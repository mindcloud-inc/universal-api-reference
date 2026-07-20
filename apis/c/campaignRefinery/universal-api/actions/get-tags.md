# Campaign Refinery: Get Tags

Retrieves all tags from Campaign Refinery.

```
GET https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Refinery `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignRefinery/latest/actions/get-tags?${params}`, {
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
      "parent_tag_id": 1,
      "tag_created_dts": "2026-05-07T12:00:00.000Z",
      "tag_id": 1,
      "tag_name": "Ava Chen",
      "tag_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `parent_tag_id` | number | Parent tag ID when the tag is nested. |
| `tag_created_dts` | date | Tag creation timestamp. |
| `tag_id` | number | Campaign Refinery numeric tag ID. |
| `tag_name` | string | Tag name. |
| `tag_uuid` | string | Campaign Refinery tag UUID. |

## Native endpoint

Through the native Campaign Refinery API, this operation is `GET /tags/get-tags` (base URL `https://app.campaignrefinery.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tags.md) for the provider-specific parameters and requirements.

