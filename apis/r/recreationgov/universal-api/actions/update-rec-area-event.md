# Recreation.gov: Update Rec Area Event

Updates a recreation area event in Recreation.gov.

```
PUT https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-rec-area-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-rec-area-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen",
  "eventId": 1,
  "registrationRequired": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-rec-area-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen",
    "eventId": 1,
    "registrationRequired": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `name` | string | yes |  |
| `description` | string | no |  |
| `eventId` | number | yes |  |
| `typeDescription` | string | no |  |
| `scopeDescription` | string | no |  |
| `frequencyRateDescription` | string | no |  |
| `feeDescription` | string | no |  |
| `ageGroup` | string | no |  |
| `registrationRequired` | boolean | yes |  |
| `adaAccess` | string | no |  |
| `comments` | string | no |  |
| `email` | string | no |  |
| `url` | string | no |  |
| `urlText` | string | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `sponsorName` | string | no |  |
| `sponsorClassType` | string | no |  |
| `sponsorPhone` | string | no |  |
| `sponsorEmail` | string | no |  |
| `sponsorUrl` | string | no |  |
| `sponsorUrlText` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "MESSAGE": "string",
      "STATUSCODE": 1,
      "SUCCESS": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `MESSAGE` | string |  |
| `STATUSCODE` | number |  |
| `SUCCESS` | boolean |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `PUT /recareas/{id}/events/{eventId}` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rec-area-event.md) for the provider-specific parameters and requirements.

