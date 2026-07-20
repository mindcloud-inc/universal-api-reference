# DecisionVault: List Questionnaires

Retrieves questionnaires from your firm in DecisionVault.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-questionnaires
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-questionnaires?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-questionnaires?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "id": "string",
      "internal_type": "string",
      "quest_approach": "string",
      "url_short_name": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `id` | string |  |
| `internal_type` | string |  |
| `quest_approach` | string |  |
| `url_short_name` | string |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /questionnaires` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-questionnaires.md) for the provider-specific parameters and requirements.

