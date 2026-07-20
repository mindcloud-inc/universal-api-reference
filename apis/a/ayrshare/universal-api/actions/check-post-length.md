# Ayrshare: Check Post Length

Checks post length against platform limits in Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/check-post-length
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/check-post-length?connectionId=$CONNECTION_ID&post=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "post": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/check-post-length?${params}`, {
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
| `post` | string | yes | Post text to calculate weighted length for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `platform` | string | no | Optional platform context for the post length check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blueskyWeightedLength": 1,
      "facebookWeightedLength": 1,
      "instagramWeightedLength": 1,
      "linkedInWeightedLength": 1,
      "tikTokWeightedLength": 1,
      "twitterValid": true,
      "twitterWeightedLength": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blueskyWeightedLength` | number | Weighted length for Bluesky. |
| `facebookWeightedLength` | number | Weighted length for Facebook. |
| `instagramWeightedLength` | number | Weighted length for Instagram. |
| `linkedInWeightedLength` | number | Weighted length for LinkedIn. |
| `tikTokWeightedLength` | number | Weighted length for TikTok. |
| `twitterValid` | boolean | Whether text is valid for X/Twitter length. |
| `twitterWeightedLength` | number | Weighted length for X/Twitter. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /post/checkPostWeight` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-post-length.md) for the provider-specific parameters and requirements.

