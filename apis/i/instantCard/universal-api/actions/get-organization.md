# InstantCard: Get Organization

Retrieves an organization from InstantCard by ID.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=20003827" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "20003827"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-organization?${params}`, {
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
| `organizationId` | number | yes | Organization ID from InstantCard. Example: `20003827`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "settings": {},
      "total_cards": 1,
      "total_templates": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Organization ID. |
| `name` | string | Organization name. |
| `settings` | object | Organization settings payload. |
| `total_cards` | number | Total cards in the organization. |
| `total_templates` | number | Total templates in the organization. |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

