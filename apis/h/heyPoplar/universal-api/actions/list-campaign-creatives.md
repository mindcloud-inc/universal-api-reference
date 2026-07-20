# HeyPoplar: List Campaign Creatives

Retrieves creatives for a HeyPoplar campaign.

```
GET https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/list-campaign-creatives
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/list-campaign-creatives?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/list-campaign-creatives?${params}`, {
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
| `campaignId` | string | yes | ID of the campaign whose creatives should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creative_type": "string",
      "default": true,
      "format": "string",
      "id": "string",
      "image_formats": "string",
      "mail_type": "string",
      "merge_tags": {},
      "name": "Ava Chen",
      "thumbnail_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creative_type` | string | Creative type from the official Poplar campaign creatives response example. |
| `default` | boolean | Whether the creative is the default creative in the official Poplar campaign creatives response example. |
| `format` | string | File format from the official Poplar campaign creatives response example. |
| `id` | string | Creative identifier from the official Poplar campaign creatives response example. |
| `image_formats` | string | Image format summary from the official Poplar campaign creatives response example. |
| `mail_type` | string | Mail type from the official Poplar campaign creatives response example. |
| `merge_tags` | object | Merge tag object from the official Poplar campaign creatives response example. |
| `name` | string | Creative name from the official Poplar campaign creatives response example. |
| `thumbnail_url` | string | Thumbnail URL from the official Poplar campaign creatives response example. |

## Native endpoint

Through the native HeyPoplar API, this operation is `GET /campaign/:id/creatives` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-creatives.md) for the provider-specific parameters and requirements.

