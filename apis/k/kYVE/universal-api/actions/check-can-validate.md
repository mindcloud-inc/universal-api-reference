# KYVE: Check Can Validate



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/check-can-validate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/check-can-validate?connectionId=$CONNECTION_ID&poolId=string&poolAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "poolId": "string",
  "poolAddress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/check-can-validate?${params}`, {
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
| `poolId` | string | yes | Pool ID to check validation against. |
| `poolAddress` | string | yes | Pool address to validate. |

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

Through the native KYVE API, this operation is `GET /kyve/query/v1beta1/can_validate/{pool_id}/{pool_address}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-can-validate.md) for the provider-specific parameters and requirements.

