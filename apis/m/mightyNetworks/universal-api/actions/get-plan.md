# Mighty Networks: Get Plan

Retrieves a plan from Mighty Networks.

```
GET https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-plan?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D&id=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkId": "{{credentials.networkId}}",
  "id": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/get-plan?${params}`, {
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
| `networkId` | string | yes | The Mighty Networks network ID or subdomain for the request path. Default: `{{credentials.networkId}}`. |
| `id` | number | yes | The ID of the plan to retrieve. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "external": true,
      "id": 1,
      "multiple": true,
      "name": "Ava Chen",
      "permalink": "https://example.com",
      "pricingType": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibleToMembers": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `external` | boolean |  |
| `id` | number |  |
| `multiple` | boolean |  |
| `name` | string |  |
| `permalink` | string |  |
| `pricingType` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `visibleToMembers` | boolean |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `GET /networks/:network_id/plans/:id/` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plan.md) for the provider-specific parameters and requirements.

