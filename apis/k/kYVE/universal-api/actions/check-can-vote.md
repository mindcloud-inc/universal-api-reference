# KYVE: Check Can Vote



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/check-can-vote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/check-can-vote?connectionId=$CONNECTION_ID&poolId=string&staker=string&voter=string&storageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "poolId": "string",
  "staker": "string",
  "voter": "string",
  "storageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/check-can-vote?${params}`, {
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
| `poolId` | string | yes | Pool ID to check voting against. |
| `staker` | string | yes | Staker address. |
| `voter` | string | yes | Voter address. |
| `storageId` | string | yes | Storage ID of the bundle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "possible": true,
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `possible` | boolean |  |
| `reason` | string |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/query/v1beta1/can_vote/{pool_id}/{staker}/{voter}/{storage_id}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-can-vote.md) for the provider-specific parameters and requirements.

