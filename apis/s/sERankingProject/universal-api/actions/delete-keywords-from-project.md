# SE Ranking Project: Delete Keywords from Project

Deletes project keywords from SE Ranking.

```
DELETE https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/delete-keywords-from-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/delete-keywords-from-project?connectionId=$CONNECTION_ID&site_id=1&keywords_ids%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site_id": "1",
  "keywords_ids[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/delete-keywords-from-project?${params}`, {
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
| `keywords_ids[]` | array<number> | yes | Array of keyword IDs to delete. |

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

Through the native SE Ranking Project API, this operation is `DELETE /sites/:site_id/keywords` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-keywords-from-project.md) for the provider-specific parameters and requirements.

