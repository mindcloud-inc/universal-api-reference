# Workiz: Create Job

Creates a new job in Workiz.

```
POST https://connect.mindcloud.co/v1/universal/workiz/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workiz/latest/actions/create-job', {
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
| `email` | string | no | Customer email address. |
| `firstName` | string | no | Customer first name. |
| `jobDateTime` | string | no | Job start date and time. |
| `jobEndDateTime` | string | no | Job end date and time. |
| `jobNotes` | string | no | Job notes. |
| `jobSource` | string | no | Job source. |
| `jobType` | string | no | Job type. |
| `lastName` | string | no | Customer last name. |
| `phone` | string | no | Primary phone number. |
| `phoneExt` | string | no | Primary phone extension. |
| `postalCode` | string | no | Postal code. |
| `referralCompany` | string | no | Referral company. |
| `secondPhone` | string | no | Secondary phone number. |
| `secondPhoneExt` | string | no | Secondary phone extension. |
| `serviceArea` | string | no | Service area. |
| `state` | string | no | State or region. |
| `timezone` | string | no | Job timezone. |
| `unit` | string | no | Unit, suite, or apartment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "link": "https://example.com",
      "serialId": "string",
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
| `serialId` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Workiz API, this operation is `POST /job/create/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

