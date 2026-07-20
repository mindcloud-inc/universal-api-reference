# Planet Money Podcast: Get Podcast Episode Page

Retrieves a Planet Money episode page from NPR.

```
GET https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-podcast-episode-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planet Money Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-podcast-episode-page?connectionId=$CONNECTION_ID&year=2026&month=03&day=20&storyId=nx-s1-5751177&slug=book-deal-proposal-auction-publishing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026",
  "month": "03",
  "day": "20",
  "storyId": "nx-s1-5751177",
  "slug": "book-deal-proposal-auction-publishing"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planetMoneyPodcast/latest/actions/get-podcast-episode-page?${params}`, {
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
| `year` | string | yes | Four-digit year from the canonical NPR episode URL. Example: `2026`. |
| `month` | string | yes | Two-digit month from the canonical NPR episode URL. Example: `03`. |
| `day` | string | yes | Two-digit day from the canonical NPR episode URL. Example: `20`. |
| `storyId` | string | yes | NPR story identifier segment from the canonical episode URL. Example: `nx-s1-5751177`. |
| `slug` | string | yes | Trailing slug segment from the canonical NPR episode URL. Example: `book-deal-proposal-auction-publishing`. |

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
| `data` | object | Raw HTML returned by the public Planet Money episode page as a Buffer-shaped object. |
| `data.data` | array<number> | HTML bytes returned by NPR. |
| `data.type` | string | Buffer type marker. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Planet Money Podcast API, this operation is `GET https://www.npr.org/:year/:month/:day/:storyId/:slug` (base URL `https://feeds.npr.org/510289`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-episode-page.md) for the provider-specific parameters and requirements.

