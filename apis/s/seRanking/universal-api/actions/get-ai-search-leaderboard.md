# SE Ranking Data: Get AI search leaderboard

Retrieves the AI search leaderboard from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-ai-search-leaderboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-ai-search-leaderboard?connectionId=$CONNECTION_ID&competitors=%5Bobject%20Object%5D&engines=chatgpt%2Cai_overview&primaryTarget=seranking.com&scope=domain&source=us" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "competitors": "[object Object]",
  "engines": "chatgpt,ai_overview",
  "primaryTarget": "seranking.com",
  "scope": "domain",
  "source": "us"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-ai-search-leaderboard?${params}`, {
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
| `competitors` | list<object> | yes | Competitor objects array with target and optional brand. Example: `[object Object]`. |
| `engines` | list<string> | yes | One or more engines (for example: chatgpt, ai_overview). One of: `ai_overview`, `chatgpt`. Example: `chatgpt,ai_overview`. |
| `primaryBrand` | string | no | Optional primary brand label. Example: `SE Ranking`. |
| `primaryTarget` | string | yes | Primary target domain/URL. Example: `seranking.com`. |
| `scope` | list<string> | yes | Scope value (for example: domain). One of: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. Example: `domain`. |
| `source` | string | yes | Regional source code (for example: us). Example: `us`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leaderboard": [
        {
          "brandPresence": 1,
          "domain": "string",
          "isPrimaryTarget": true,
          "linkPresence": 1,
          "rank": 1,
          "shareOfVoice": 1
        }
      ],
      "requestMetadata": {
        "competitors": [
          "string"
        ],
        "engines": [
          "string"
        ],
        "primary": "string",
        "source": "string"
      },
      "results": {
        "semrush": {
          "com": {
            "chatgpt": {
              "brandPresence": 1,
              "linkPresence": 1
            }
          }
        },
        "seranking": {
          "com": {
            "chatgpt": {
              "brandPresence": 1,
              "linkPresence": 1
            }
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leaderboard` | array<object> | Ranked leaderboard rows for compared domains. |
| `leaderboard[].brandPresence` | number |  |
| `leaderboard[].domain` | string |  |
| `leaderboard[].isPrimaryTarget` | boolean |  |
| `leaderboard[].linkPresence` | number |  |
| `leaderboard[].rank` | number |  |
| `leaderboard[].shareOfVoice` | number |  |
| `requestMetadata` | object | Echoed request metadata used by leaderboard calculation. |
| `requestMetadata.competitors` | array<string> |  |
| `requestMetadata.engines` | array<string> |  |
| `requestMetadata.primary` | string |  |
| `requestMetadata.source` | string |  |
| `results` | object | Per-domain per-engine breakdown of brand/link presence. |
| `results.semrush.com` | object |  |
| `results.semrush.com.chatgpt` | object |  |
| `results.semrush.com.chatgpt.brandPresence` | number |  |
| `results.semrush.com.chatgpt.linkPresence` | number |  |
| `results.seranking.com` | object |  |
| `results.seranking.com.chatgpt` | object |  |
| `results.seranking.com.chatgpt.brandPresence` | number |  |
| `results.seranking.com.chatgpt.linkPresence` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `POST /ai-search/overview/leaderboard` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ai-search-leaderboard.md) for the provider-specific parameters and requirements.

