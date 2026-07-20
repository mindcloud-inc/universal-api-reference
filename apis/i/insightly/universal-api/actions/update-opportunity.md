# Insightly: Update Opportunity

Updates an existing opportunity in Insightly.

```
PUT https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunityId": 1,
  "opportunityName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-opportunity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunityId": 1,
    "opportunityName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opportunityId` | number | yes | The Opportunity ID to update. |
| `opportunityName` | string | yes | The opportunity name. |
| `opportunityState` | string | no | The opportunity state. |
| `bidAmount` | number | no | The bid amount for the opportunity. |
| `bidCurrency` | string | no | The bid currency code. |
| `forecastCloseDate` | string | no | The forecast close date in UTC. |
| `organisationId` | number | no | The related Organisation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualCloseDate": "2026-05-07T12:00:00.000Z",
      "bidAmount": 1,
      "bidCurrency": "string",
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "forecastCloseDate": "2026-05-07T12:00:00.000Z",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "opportunityDetails": "string",
      "opportunityId": 1,
      "opportunityName": "Ava Chen",
      "opportunityState": "string",
      "organisationId": 1,
      "ownerUserId": 1,
      "pipelineId": 1,
      "probability": 1,
      "responsibleUserId": 1,
      "stageId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualCloseDate` | date |  |
| `bidAmount` | number |  |
| `bidCurrency` | string |  |
| `createdUserId` | number |  |
| `dateCreatedUtc` | date |  |
| `dateUpdatedUtc` | date |  |
| `forecastCloseDate` | date |  |
| `lastActivityDateUtc` | date |  |
| `nextActivityDateUtc` | date |  |
| `opportunityDetails` | string |  |
| `opportunityId` | number |  |
| `opportunityName` | string |  |
| `opportunityState` | string |  |
| `organisationId` | number |  |
| `ownerUserId` | number |  |
| `pipelineId` | number |  |
| `probability` | number |  |
| `responsibleUserId` | number |  |
| `stageId` | number |  |

## Native endpoint

Through the native Insightly API, this operation is `PUT {{credentials.apiBaseUrl}}Opportunities` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-opportunity.md) for the provider-specific parameters and requirements.

