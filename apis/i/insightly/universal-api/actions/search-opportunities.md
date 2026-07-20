# Insightly: Search Opportunities

Finds opportunities in Insightly by search filters.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-opportunities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-opportunities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldName` | string | no | Filter opportunities by this field name. |
| `fieldValue` | string | no | Filter opportunities by this field value. |
| `updatedAfterUtc` | string | no | Return opportunities updated after this UTC timestamp. |
| `brief` | boolean | no | Return only top-level properties for each opportunity. |
| `countTotal` | boolean | no | Return the total-record count in the response headers. |

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

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Opportunities/Search` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-opportunities.md) for the provider-specific parameters and requirements.

