# HirePOS: Create Lead

Creates a new lead in HirePOS.

```
POST https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HirePOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/create-lead', {
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
| `addressLine1` | string | no | Primary lead address line. |
| `addressLine2` | string | no | Secondary lead address line. |
| `city` | string | no | Lead city. |
| `company` | string | no | Lead company name. |
| `email` | string | no | Lead email address. |
| `fax` | string | no | Lead fax number. |
| `firstName` | string | no | Lead first name. |
| `lastName` | string | no | Lead last name. |
| `notes` | string | no | Additional lead notes. |
| `phone1` | string | no | Primary lead phone number. |
| `phone2` | string | no | Secondary lead phone number. |
| `phone3` | string | no | Third lead phone number. |
| `postcode` | string | no | Lead postcode. |
| `state` | string | no | Lead state. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": "string",
      "errorRaised": "string",
      "errorType": "string",
      "leads": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | string | HirePOS error message when the lead create request fails. |
| `errorRaised` | string | Whether HirePOS raised an error for the lead create request. |
| `errorType` | string | HirePOS error type when the lead create request fails. |
| `leads` | array<object> | Lead records returned by HirePOS after the create request. |

## Native endpoint

Through the native HirePOS API, this operation is `POST /Leads` (base URL `https://api.hirepos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

