# InstantCard: Create Address

Creates a new address in InstantCard.

```
POST https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "20003827",
  "address1": "418 Highland Rd.",
  "country": "USA",
  "city": "Feasterville",
  "state": "PA",
  "zipCode": "19053",
  "contactFullName": "MindCloud Address Bot",
  "contactEmail": "api+address@instantcard.net"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/create-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "20003827",
    "address1": "418 Highland Rd.",
    "country": "USA",
    "city": "Feasterville",
    "state": "PA",
    "zipCode": "19053",
    "contactFullName": "MindCloud Address Bot",
    "contactEmail": "api+address@instantcard.net"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes | Organization ID from InstantCard. Example: `20003827`. |
| `organizationName` | string | no | Organization name for the address. Example: `InstantCard API`. |
| `label` | string | no | Address label. Example: `MindCloud Staging Address`. |
| `primary` | boolean | no | Whether this is the primary address. Example: `false`. |
| `address1` | string | yes | Address line 1. Example: `418 Highland Rd.`. |
| `address2` | string | no | Address line 2. Example: `Suite 100`. |
| `country` | string | yes | Country. Example: `USA`. |
| `city` | string | yes | City. Example: `Feasterville`. |
| `state` | string | yes | State or province code. Example: `PA`. |
| `zipCode` | string | yes | Postal code. Example: `19053`. |
| `contactFullName` | string | yes | Full name for the linked contact. Example: `MindCloud Address Bot`. |
| `contactEmail` | string | yes | Email for the linked contact. Example: `api+address@instantcard.net`. |
| `contactPhoneNumber` | string | no | Phone number for the linked contact. Example: `555-450-9908`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | no | Existing contact ID to link to this address. Example: `12629`. |

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

Through the native InstantCard API, this operation is `POST /api/v2/organizations/:organizationId/addresses` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-address.md) for the provider-specific parameters and requirements.

