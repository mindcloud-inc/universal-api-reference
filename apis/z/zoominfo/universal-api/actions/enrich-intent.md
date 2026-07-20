# Zoominfo: Enrich Intent

Enriches company intent data with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-intent?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-intent?${params}`, {
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
| `topics[]` | array<string> | no | Intent topics. Accepts an Array of up to 50 Strings. See the 'Intent Topics' endpoint for values. Accepts multiple values as an array. |
| `signalStartDate` | string | no | Start date for a company signaling interest in a topic |
| `signalEndDate` | string | no | End date for a company signaling interest in a topic |
| `signalScoreMin` | number | no | Minimum signal score. Use with signalScoreMax to form a range. Minimum score is 60 and maximum is 100. |
| `signalScoreMax` | number | no | Maximum signal score. Use with signalScoreMin to form a range. Minimum score is 60 and maximum is 100. |
| `audienceStrengthMin` | string | no | Minimum audience strength score. Use with audienceStrengthMax to form a range. Values are A, B, C, D, and E, with A indicating a larger audience. |
| `audienceStrengthMax` | string | no | Maximum audience strength score. Use with audienceStrengthMin to form a range. Values are A, B, C, D, and E, with A indicating a larger audience. |
| `findRecommendedContacts` | boolean | no | Flag to indicate whether recommended contacts should be fetched in result or not. Default is true |
| `companyId` | number | no | Unique ZoomInfo identifier for a company |
| `companyName` | string | no | Company name |
| `companyWebsite` | string | no | The website of the company you are searching for |
| `sortBy` | string | no | Sorts results by valid output fields |
| `sortOrder` | string | no | Default value is desc. It accepts the following values { Asc, Ascending, desc, descending } |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audienceStrength": "string",
      "category": "string",
      "company": {
        "hasOtherTopicConsumption": true,
        "id": 1,
        "name": "Ava Chen",
        "website": "string"
      },
      "id": "string",
      "recommendedContacts": [
        {}
      ],
      "signalDate": "string",
      "signalScore": 1,
      "spikesInDateRange": 1,
      "topic": "string",
      "topSignalLocations": [
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
| `audienceStrength` | string |  |
| `category` | string |  |
| `company.hasOtherTopicConsumption` | boolean |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `company.website` | string |  |
| `id` | string |  |
| `recommendedContacts` | array<object> |  |
| `signalDate` | string |  |
| `signalScore` | number |  |
| `spikesInDateRange` | number |  |
| `topic` | string |  |
| `topSignalLocations` | array<object> |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/intent` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/enrich-intent.md) for the provider-specific parameters and requirements.

