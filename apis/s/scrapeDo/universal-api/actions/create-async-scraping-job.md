# Scrape do: Create async scraping job

Creates a new async scraping job in Scrape do.

```
POST https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/create-async-scraping-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/create-async-scraping-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targets[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/create-async-scraping-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targets[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `geoCode` | string | no | Country code for geo-targeting async jobs. |
| `method` | string | no | HTTP method to use for each target request. |
| `targets[]` | array<string> | yes | One or more URLs to scrape asynchronously. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "JobID": "string",
      "Message": "string",
      "TaskIDs": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `JobID` | string | Created job identifier. |
| `Message` | string | Creation status message. |
| `TaskIDs` | array<string> | Created task identifiers. |

## Native endpoint

Through the native Scrape do API, this operation is `POST https://q.scrape.do/api/v1/jobs` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-async-scraping-job.md) for the provider-specific parameters and requirements.

