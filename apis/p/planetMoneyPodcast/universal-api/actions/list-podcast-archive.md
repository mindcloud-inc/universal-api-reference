# Planet Money Podcast: List Podcast Archive

Retrieves older Planet Money episode listings from NPR.

```
GET https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/list-podcast-archive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planet Money Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/list-podcast-archive?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/list-podcast-archive?${params}`, {
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
| `start` | number | no | Offset used by NPR's archive partials endpoint. Use larger values like 10, 20, or 30 to page deeper into older episodes. Default: `0`. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "data": [
          1
        ],
        "type": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw HTML returned by the public Planet Money archive page as a Buffer-shaped object. |
| `data.data` | array<number> | HTML bytes returned by NPR. |
| `data.type` | string | Buffer type marker. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Planet Money Podcast API, this operation is `GET https://www.npr.org/podcasts/510289/planet-money/partials` (base URL `https://feeds.npr.org/510289`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-podcast-archive.md) for the provider-specific parameters and requirements.

