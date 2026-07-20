# SE Ranking Data: Get prompts by brand

Retrieves prompts by brand from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-prompts-by-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-prompts-by-brand?connectionId=$CONNECTION_ID&brand=seranking&engine=chatgpt&source=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "brand": "seranking",
  "engine": "chatgpt",
  "source": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-prompts-by-brand?${params}`, {
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
| `brand` | string | yes | Brand identifier or name. Example: `seranking`. |
| `endDate` | string | no | End date in YYYY-MM-DD format. |
| `engine` | list<string> | yes | Engine identifier (for example: chatgpt). One of: `ai_overview`, `chatgpt`. Example: `chatgpt`. |
| `fields` | string | no | Comma-separated fields to include. |
| `sort` | string | no | Comma-separated sort fields with direction (for example: date:desc). |
| `source` | string | yes | Regional source code (for example: us). Example: `us`. |
| `startDate` | string | no | Start date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "prompts": [
        {
          "answer": {
            "links": [
              "https://example.com"
            ],
            "text": "string"
          },
          "prompt": "string",
          "type": "string",
          "volume": 1
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string | Snapshot/reporting date. |
| `prompts` | array<object> | Prompt rows with answer metadata. |
| `prompts[].answer` | object |  |
| `prompts[].answer.links` | array<string> |  |
| `prompts[].answer.text` | string |  |
| `prompts[].prompt` | string |  |
| `prompts[].type` | string |  |
| `prompts[].volume` | number |  |
| `total` | number | Total matching prompts. |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /ai-search/prompts-by-brand` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prompts-by-brand.md) for the provider-specific parameters and requirements.

