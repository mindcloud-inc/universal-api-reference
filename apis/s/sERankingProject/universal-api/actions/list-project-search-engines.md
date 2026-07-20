# SE Ranking Project: List Project Search Engines

Retrieves search engine configurations for a project in SE Ranking.

```
GET https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-project-search-engines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-project-search-engines?connectionId=$CONNECTION_ID&site_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-project-search-engines?${params}`, {
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
| `site_id` | list<number> | yes | Project site identifier from SE Ranking. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "keywordCount": 1,
        "langCode": "string",
        "mergeMap": 1,
        "paidResults": 1,
        "regionId": 1,
        "searchEngineId": 1,
        "siteEngineId": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item` | object |  |
| `item.keywordCount` | number |  |
| `item.langCode` | string |  |
| `item.mergeMap` | number |  |
| `item.paidResults` | number |  |
| `item.regionId` | number |  |
| `item.searchEngineId` | number |  |
| `item.siteEngineId` | number |  |

## Native endpoint

Through the native SE Ranking Project API, this operation is `GET /sites/:site_id/search-engines` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-search-engines.md) for the provider-specific parameters and requirements.

