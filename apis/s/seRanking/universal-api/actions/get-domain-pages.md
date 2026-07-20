# SE Ranking Data: Get domain pages

Retrieves domain pages from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-pages?connectionId=$CONNECTION_ID&scope=domain&source=us&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scope": "domain",
  "source": "us",
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-domain-pages?${params}`, {
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
| `scope` | list<string> | yes | Analysis scope (for example: domain). One of: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. Example: `domain`. |
| `source` | string | yes | Regional database code (for example: us). Example: `us`. |
| `target` | string | yes | Target domain or URL (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "intents": {
        "c": {
          "count": 1,
          "percents": 1,
          "traffic": 1
        },
        "i": {
          "count": 1,
          "percents": 1,
          "traffic": 1
        },
        "l": {
          "count": 1,
          "percents": 1,
          "traffic": 1
        },
        "n": {
          "count": 1,
          "percents": 1,
          "traffic": 1
        },
        "t": {
          "count": 1,
          "percents": 1,
          "traffic": 1
        }
      },
      "keywordsCount": 1,
      "priceSum": 1,
      "title": "string",
      "trafficPercent": 1,
      "trafficSum": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `intents` | object |  |
| `intents.c` | object |  |
| `intents.c.count` | number |  |
| `intents.c.percents` | number |  |
| `intents.c.traffic` | number |  |
| `intents.i` | object |  |
| `intents.i.count` | number |  |
| `intents.i.percents` | number |  |
| `intents.i.traffic` | number |  |
| `intents.l` | object |  |
| `intents.l.count` | number |  |
| `intents.l.percents` | number |  |
| `intents.l.traffic` | number |  |
| `intents.n` | object |  |
| `intents.n.count` | number |  |
| `intents.n.percents` | number |  |
| `intents.n.traffic` | number |  |
| `intents.t` | object |  |
| `intents.t.count` | number |  |
| `intents.t.percents` | number |  |
| `intents.t.traffic` | number |  |
| `keywordsCount` | number |  |
| `priceSum` | number |  |
| `title` | string |  |
| `trafficPercent` | number |  |
| `trafficSum` | number |  |
| `url` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /domain/pages` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-pages.md) for the provider-specific parameters and requirements.

