# Workiz: Update Lead

Updates an existing lead in Workiz.

```
PUT https://connect.mindcloud.co/v1/universal/workiz/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiz/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
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
| `leadNotes` | string | no | Lead notes. |
| `phone` | string | no | Primary phone number. |
| `phoneExt` | string | no | Primary phone extension. |
| `postalCode` | string | no | Postal code. |
| `secondPhone` | string | no | Secondary phone number. |
| `secondPhoneExt` | string | no | Secondary phone extension. |
| `serviceArea` | string | no | Service area. |
| `state` | string | no | State or region. |
| `status` | string | no | Lead status. |
| `tags[]` | array<string> | no | Lead tags. |
| `timezone` | string | no | Lead timezone. |
| `unit` | string | no | Unit, suite, or apartment. |
| `uuid` | string | yes | The lead UUID to update. |

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

Through the native Workiz API, this operation is `POST /lead/update/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

