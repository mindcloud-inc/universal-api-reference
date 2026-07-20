# Workiz: Create Lead

Creates a new lead in Workiz.

```
POST https://connect.mindcloud.co/v1/universal/workiz/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiz/latest/actions/create-lead', {
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
| `address` | string | no | Street address. |
| `city` | string | no | City. |
| `clientId` | number | no | Existing Workiz client ID. |
| `company` | string | no | Company name. |
| `country` | string | no | Country code or name. |
| `email` | string | no | Lead email address. |
| `firstName` | string | no | Lead first name. |
| `jobSource` | string | no | Lead source. |
| `jobType` | string | no | Lead job type. |
| `lastName` | string | no | Lead last name. |
| `leadDateTime` | string | no | Lead start date and time. |
| `leadEndDateTime` | string | no | Lead end date and time. |
| `leadLost` | number | no | Lead lost flag. |
| `leadNotes` | string | no | Lead notes. |
| `phone` | string | no | Primary phone number. |
| `phoneExt` | string | no | Primary phone extension. |
| `postalCode` | string | no | Postal code. |
| `referralCompany` | string | no | Referral company. |
| `secondPhone` | string | no | Secondary phone number. |
| `secondPhoneExt` | string | no | Secondary phone extension. |
| `serviceArea` | string | no | Service area. |
| `state` | string | no | State or region. |
| `timezone` | string | no | Lead timezone. |
| `unit` | string | no | Unit, suite, or apartment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "link": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string |  |
| `link` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Workiz API, this operation is `POST /lead/create/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

