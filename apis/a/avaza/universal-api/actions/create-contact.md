# Avaza: Create Contact

Creates a new contact in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactemail": "ava@example.com",
  "firstname": "Ava",
  "lastname": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactemail": "ava@example.com",
    "firstname": "Ava",
    "lastname": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyidfk` | number | no |  |
| `companyname` | string | no |  |
| `currencycode` | string | no |  |
| `companybillingaddress` | string | no |  |
| `companybillingaddressline` | string | no |  |
| `companybillingaddresscity` | string | no |  |
| `companybillingaddressstate` | string | no |  |
| `companybillingaddresspostcode` | string | no |  |
| `companybillingaddresscountrycode` | string | no |  |
| `contactemail` | string | yes |  |
| `firstname` | string | yes |  |
| `lastname` | string | yes |  |
| `positiontitle` | string | no |  |
| `mobile` | string | no |  |
| `phone` | string | no |  |
| `updateexisting` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/Contact` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

