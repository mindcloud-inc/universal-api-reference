# Planet Money Podcast: Get Podcast Show Page

Retrieves the Planet Money show page from NPR.

```
GET https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-podcast-show-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planet Money Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-podcast-show-page?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-podcast-show-page?${params}`, {
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
| `data` | object | Raw HTML returned by the public Planet Money show page as a Buffer-shaped object. |
| `data.data` | array<number> | HTML bytes returned by NPR. |
| `data.type` | string | Buffer type marker. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Planet Money Podcast API, this operation is `GET https://www.npr.org/podcasts/510289/planet-money` (base URL `https://feeds.npr.org/510289`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-show-page.md) for the provider-specific parameters and requirements.

