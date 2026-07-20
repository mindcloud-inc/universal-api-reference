# KYVE: Get Current Vote Status



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-current-vote-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-current-vote-status?connectionId=$CONNECTION_ID&poolId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "poolId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-current-vote-status?${params}`, {
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
| `poolId` | string | yes | Pool ID to query current vote status for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abstain": "string",
      "invalid": "string",
      "total": "string",
      "valid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abstain` | string |  |
| `invalid` | string |  |
| `total` | string |  |
| `valid` | string |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/query/v1beta1/current_vote_status/{pool_id}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-vote-status.md) for the provider-specific parameters and requirements.

