# FuseDesk: Create Contact

Creates a new contact in FuseDesk.

```
POST https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FuseDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fuseDesk/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cityBilling` | string | no | Billing city. |
| `company` | string | no | Company name. |
| `countryBilling` | string | no | Billing country. |
| `emailAddress` | string | no | Primary email address. |
| `emailAddress2` | string | no | Secondary email address. |
| `emailAddress3` | string | no | Tertiary email address. |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | no | Contact last name. |
| `phone1` | string | no | Primary phone number. |
| `phone2` | string | no | Secondary phone number. |
| `phoneExt1` | string | no | Primary phone extension. |
| `phoneExt2` | string | no | Secondary phone extension. |
| `postalBilling` | string | no | Billing postal code. |
| `stateBilling` | string | no | Billing state or region. |
| `street1Billing` | string | no | Billing street address line 1. |
| `street2Billing` | string | no | Billing street address line 2. |
| `timeZone` | string | no | Time zone identifier. |
| `website` | string | no | Website URL. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FuseDesk API returns.

## Native endpoint

Through the native FuseDesk API, this operation is `POST /api/v2/contacts` (base URL `https://{{credentials.appName}}.fusedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

