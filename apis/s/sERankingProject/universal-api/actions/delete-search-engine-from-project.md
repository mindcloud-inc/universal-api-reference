# SE Ranking Project: Delete Search Engine From Project

Deletes a project search engine from SE Ranking.

```
DELETE https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/delete-search-engine-from-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/delete-search-engine-from-project?connectionId=$CONNECTION_ID&site_engine_id=1&site_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site_engine_id": "1",
  "site_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/delete-search-engine-from-project?${params}`, {
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
| `site_engine_id` | number | yes |  |
| `site_id` | list<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. The saved successful response was an empty string (HTTP 204). |

## Native endpoint

Through the native SE Ranking Project API, this operation is `DELETE /sites/:site_id/search-engines/:site_engine_id` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-search-engine-from-project.md) for the provider-specific parameters and requirements.

