# SE Ranking Project: List Website Keywords

Retrieves project keywords and basic statistics from SE Ranking.

```
GET https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-website-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-website-keywords?connectionId=$CONNECTION_ID&site_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/list-website-keywords?${params}`, {
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
        "groupId": "string",
        "id": "string",
        "name": "Ava Chen",
        "siteEngineIds": [
          1
        ],
        "tags": [
          "string"
        ]
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
| `item.groupId` | string |  |
| `item.id` | string |  |
| `item.name` | string |  |
| `item.siteEngineIds` | array<number> |  |
| `item.tags` | array<string> |  |

## Native endpoint

Through the native SE Ranking Project API, this operation is `GET /sites/:site_id/keywords` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-website-keywords.md) for the provider-specific parameters and requirements.

