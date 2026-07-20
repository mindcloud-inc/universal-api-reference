# Zoominfo: List Intent

Finds intent-based companies and contacts in ZoomInfo.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-intent?connectionId=$CONNECTION_ID&limit=25&offset=0&topics%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "topics[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-intent?${params}`, {
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
| `topics[]` | array<string> | yes | Accepts multiple values as an array. |
| `signalScoreMin` | number | no | Minimum signal score. |
| `signalScoreMax` | number | no | Maximum signal score. |
| `audienceStrengthMin` | string | no | Minimum audience strength score. |
| `audienceStrengthMax` | string | no | Maximum audience strength score. |
| `metroRegion` | string | no | Company metro area. |
| `industryCodes` | string | no | Top-level industry codes. |
| `sortBy` | string | no | Sort results by a valid output field. |
| `sortOrder` | string | no | Sort direction. |

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
      "newSignal": true,
      "recommendedContacts": [
        {
          "firstName": "Ava",
          "id": 1,
          "jobFunction": [
            {
              "department": "string",
              "name": "Ava Chen"
            }
          ],
          "jobTitle": "string",
          "lastName": "Chen"
        }
      ],
      "signalDate": "string",
      "signalScore": 1,
      "topic": "string",
      "trend": 1
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
| `newSignal` | boolean |  |
| `recommendedContacts[].firstName` | string |  |
| `recommendedContacts[].id` | number |  |
| `recommendedContacts[].jobFunction[].department` | string |  |
| `recommendedContacts[].jobFunction[].name` | string |  |
| `recommendedContacts[].jobTitle` | string |  |
| `recommendedContacts[].lastName` | string |  |
| `signalDate` | string |  |
| `signalScore` | number |  |
| `topic` | string |  |
| `trend` | number |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST search/intent` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-intent.md) for the provider-specific parameters and requirements.

