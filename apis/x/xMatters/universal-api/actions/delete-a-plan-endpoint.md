# xMatters: Delete a plan endpoint

Deletes a plan endpoint from your xMatters instance.

```
DELETE https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-plan-endpoint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-plan-endpoint?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/delete-a-plan-endpoint?${params}`, {
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
| `endpointId` | string | no |  |
| `planId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticationType": "string",
      "endpointType": "string",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "plan": {
        "id": "string"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationType` | string |  |
| `endpointType` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `plan.id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `DELETE plans/{planId}/endpoints/{endpointId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-plan-endpoint.md) for the provider-specific parameters and requirements.

