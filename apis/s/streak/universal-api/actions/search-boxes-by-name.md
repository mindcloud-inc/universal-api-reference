# Streak: Search Boxes By Name

Finds boxes in Streak by exact name.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/search-boxes-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/search-boxes-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/search-boxes-by-name?${params}`, {
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
| `name` | string | yes | Exact box name to search for. |
| `pipelineKey` | string<string> | no | Limit box results to one or more pipelines. Accepts multiple values as an array. |
| `stageKey` | string<string> | no | Limit box results to one or more stages. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "results": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number | The current search results page. |
| `results` | object | The box search results grouped under results.boxes. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v1/search` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-boxes-by-name.md) for the provider-specific parameters and requirements.

