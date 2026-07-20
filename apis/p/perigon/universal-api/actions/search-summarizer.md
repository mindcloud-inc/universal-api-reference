# Perigon: Search Summarizer

Generates Perigon news summaries from a custom prompt.

```
GET https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-summarizer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perigon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-summarizer?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-summarizer?${params}`, {
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
| `prompt` | string | no | Example: `Summarize the key developments in one paragraph.`. |
| `maxArticleCount` | number | no | Example: `10`. |
| `returnedArticleCount` | number | no | Example: `5`. |
| `summarizeFields` | string | no | Accepts multiple values as an array. Example: `TITLE`. |
| `method` | string | no | Example: `ARTICLES`. |
| `model` | string | no | Example: `gpt-4.1`. |
| `temperature` | number | no | Example: `0.7`. |
| `topP` | number | no | Example: `1.0`. |
| `maxTokens` | number | no | Example: `512`. |
| `q` | string | no | Example: `renewable energy`. |
| `sortBy` | string | no | Example: `date`. |
| `size` | number | no | Example: `10`. |
| `from` | date | no | Example: `2026-04-01T00:00:00`. |
| `to` | date | no | Example: `2026-04-09T23:59:59`. |
| `source` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `reuters.com`. |
| `category` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Energy`. |
| `topic` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `Renewable Energy`. |
| `country` | string | no | Accepts multiple values in one string, delimited by `,`. Example: `us`. |
| `companyName` | string | no | Example: `Tesla`. |
| `showNumResults` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numResults": 1,
      "results": [
        {}
      ],
      "status": 1,
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numResults` | number |  |
| `results` | array<object> |  |
| `status` | number |  |
| `summary` | string |  |

## Native endpoint

Through the native Perigon API, this operation is `POST /v1/summarize` (base URL `https://api.perigon.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-summarizer.md) for the provider-specific parameters and requirements.

