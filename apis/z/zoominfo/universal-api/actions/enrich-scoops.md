# Zoominfo: Enrich Scoops

Enriches company scoops with ZoomInfo data.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-scoops
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-scoops?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/enrich-scoops?${params}`, {
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
| `companyId` | string | no | ZoomInfo unique identifier for the company. Will accept a comma-separated list. |
| `companyName` | string | no | Company name. Accepts a pipe ('\|')-separated list. |
| `companyWebsite` | string | no | Company domain. Accepts a comma-separated list. |
| `publishedStartDate` | string | no | Starting date to search for scoops based on when published. Form a range using publishedEndDate or omit publishedEndDate to search to the current date. Uses YYYY-MM-DD format. |
| `publishedEndDate` | string | no | Ending date to search for scoops based on when published. Form a range using publishedEndDate. Uses YYYY-MM-DD format. |
| `updatedSinceCreation` | boolean | no | Include scoops that have been updated since publishedStartDate |
| `scoopType` | string | no | Retrieve scoops based on type (e.g. earnings, awards and partnerships). Accepts a comma-separated list of IDs from the endpoint: /lookup/scooptype. |
| `scoopTopic` | string | no | Retrieve scoops based on topic (e.g. integration, consolidation and compliance). Accepts a comma-separated list of IDs from the endpoint: /lookup/scooptopic. |
| `department` | string | no | Retrieve scoops based on department (e.g. IT, finance and HR). Accepts a comma-separated list of IDs from the endpoint: /lookup/scoopdepartment. |
| `scoopId` | string | no | ZoomInfo unique identifier for a scoop. Accepts a comma-separated list. |
| `description` | string | no | Search for scoops based on description. Accepts a space-separated list of individual words. |
| `sortBy` | string | no | Sorts results by valid output fields |
| `sortOrder` | string | no | Default value is desc. It accepts the following values { asc, ascending, desc, descending |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "id": 1,
        "name": "Ava Chen"
      },
      "description": "string",
      "id": 1,
      "link": "https://example.com",
      "linkText": "https://example.com",
      "originalPublishedDate": "string",
      "person": {
        "contacts": [
          "string"
        ]
      },
      "publishedDate": "string",
      "topics": [
        {}
      ],
      "types": [
        {}
      ],
      "updateText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.id` | number |  |
| `company.name` | string |  |
| `description` | string |  |
| `id` | number |  |
| `link` | string |  |
| `linkText` | string |  |
| `originalPublishedDate` | string |  |
| `person.contacts` | array<string> |  |
| `publishedDate` | string |  |
| `topics` | array<object> |  |
| `types` | array<object> |  |
| `updateText` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST enrich/scoop` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/enrich-scoops.md) for the provider-specific parameters and requirements.

