# HigherGov: List Pursuits

Retrieves authenticated pursuits from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-pursuits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-pursuits?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-pursuits?${params}`, {
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
| `referenceId` | string | no | Reference ID for the pursuit |
| `searchId` | string | no | HigherGov SearchID |
| `uniqueKey` | string | no | Unique internal pursuit key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "est_value": 1,
      "owner": "string",
      "pgo": 1,
      "pipeline_name": "Ava Chen",
      "proposal_due_date": "string",
      "pursuit_name": "Ava Chen",
      "pursuit_path": "string",
      "pwin": 1,
      "reference_id": 1,
      "stage_name": "Ava Chen",
      "unique_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `est_value` | number |  |
| `owner` | string |  |
| `pgo` | number |  |
| `pipeline_name` | string |  |
| `proposal_due_date` | string |  |
| `pursuit_name` | string |  |
| `pursuit_path` | string |  |
| `pwin` | number |  |
| `reference_id` | number |  |
| `stage_name` | string |  |
| `unique_key` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/pursuit/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pursuits.md) for the provider-specific parameters and requirements.

