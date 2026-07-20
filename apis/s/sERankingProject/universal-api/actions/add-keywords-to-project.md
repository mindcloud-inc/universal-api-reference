# SE Ranking Project: Add Keywords to Project

Adds keywords to an existing SE Ranking project.

```
POST https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/add-keywords-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/add-keywords-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site_id": 1,
  "keyword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/add-keywords-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site_id": 1,
    "keyword": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `site_id` | list<number> | yes | Project site identifier from SE Ranking. |
| `keyword` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1,
      "ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | number |  |
| `ids` | array<number> |  |

## Native endpoint

Through the native SE Ranking Project API, this operation is `POST /sites/:site_id/keywords` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-keywords-to-project.md) for the provider-specific parameters and requirements.

