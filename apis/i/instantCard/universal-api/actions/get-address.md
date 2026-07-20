# InstantCard: Get Address

Retrieves an address from InstantCard by ID.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-address?connectionId=$CONNECTION_ID&id=1&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-address?${params}`, {
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
| `id` | number | yes | Address ID from InstantCard. |
| `organizationId` | number | yes | Organization ID from InstantCard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "city": "string",
      "contact": {},
      "contact_id": 1,
      "country": "string",
      "id": 1,
      "label": "string",
      "organization_id": 1,
      "organization_name": "Ava Chen",
      "primary": true,
      "state": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string | Address line 1. |
| `address2` | string | Address line 2. |
| `city` | string | City. |
| `contact` | object | Embedded contact payload. |
| `contact_id` | number | Related contact ID. |
| `country` | string | Country. |
| `id` | number | Address ID. |
| `label` | string | Address label. |
| `organization_id` | number | Organization ID. |
| `organization_name` | string | Organization name. |
| `primary` | boolean | Whether the address is primary. |
| `state` | string | State. |
| `zip_code` | string | Postal code. |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/addresses/:id` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-address.md) for the provider-specific parameters and requirements.

