# Mighty Networks: Archive Plan

Archives a plan in Mighty Networks, canceling subscriptions and revoking access.

```
DELETE https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/archive-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/archive-plan?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkId": "{{credentials.networkId}}",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/archive-plan?${params}`, {
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
| `networkId` | string | yes | The Mighty Networks network ID. Default: `{{credentials.networkId}}`. |
| `id` | number | yes | The ID of the plan to archive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `DELETE /networks/:network_id/plans/:id/` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-plan.md) for the provider-specific parameters and requirements.

