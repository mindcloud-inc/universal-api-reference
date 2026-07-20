# Snapchat Ads: Fetch Media by IDs

Retrieves media assets from Snapchat Ads by media IDs.

```
GET https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-media-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-media-by-ids?connectionId=$CONNECTION_ID&adAccountId=string&mediaIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "string",
  "mediaIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/fetch-media-by-ids?${params}`, {
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
| `adAccountId` | string | yes | The Snapchat Ad Account ID that owns the media. |
| `mediaIds` | list<string> | yes | An array of Snapchat Media IDs to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "media": [
        {
          "media": {
            "download_link": "https://example.com",
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
          }
        }
      ],
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `media[].media.download_link` | string |  |
| `media[].media.id` | string |  |
| `media[].media.name` | string |  |
| `media[].media.type` | string |  |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Ads API, this operation is `POST /adaccounts/:adAccountId/get_media_by_ids` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-media-by-ids.md) for the provider-specific parameters and requirements.

