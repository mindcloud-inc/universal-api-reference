# InstantCard: Update Address

Updates an existing address in InstantCard.

```
PUT https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/update-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/update-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "20003827",
  "id": "73818"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/update-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "20003827",
    "id": "73818"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address1` | string | no | Address line 1. |
| `address2` | string | no | Address line 2. |
| `city` | string | no | City. |
| `contactEmail` | string | no | Email for the linked contact. |
| `contactFullName` | string | no | Full name for the linked contact. |
| `contactPhoneNumber` | string | no | Phone number for the linked contact. |
| `country` | string | no | Country. |
| `label` | string | no | Address label. |
| `organizationId` | number | yes | Organization ID from InstantCard. Example: `20003827`. |
| `organizationName` | string | no | Organization name for the address. |
| `zipCode` | string | no | Postal code. |
| `id` | number | yes | Address ID from InstantCard. Example: `73818`. |
| `primary` | boolean | no | Whether this is the primary address. Example: `false`. |
| `state` | string | no | State or province code. Example: `CO`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | no | Existing contact ID to link to this address. Example: `73932`. |

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

Through the native InstantCard API, this operation is `PATCH /api/v2/organizations/:organizationId/addresses/:id` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-address.md) for the provider-specific parameters and requirements.

