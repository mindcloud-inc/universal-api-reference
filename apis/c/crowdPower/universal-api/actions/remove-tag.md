# CrowdPower: Remove Tag

Removes a tag from a customer in CrowdPower.

```
DELETE https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/remove-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/remove-tag?connectionId=$CONNECTION_ID&customerId=string&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string",
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/remove-tag?${params}`, {
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
| `customerId` | string | yes | Customer identifier. |
| `name` | string | yes | Tag name to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer_id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer_id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native CrowdPower API, this operation is `DELETE customers/:customer_id/tags` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag.md) for the provider-specific parameters and requirements.

