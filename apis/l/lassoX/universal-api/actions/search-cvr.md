# Lasso X: Search CVR

Finds CVR companies or people in Lasso X by query.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/search-cvr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/search-cvr?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/search-cvr?${params}`, {
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
| `query` | string | yes | Search query. Supports names, CVR numbers, Lasso IDs, phone numbers, and documented filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": {
        "continuationToken": "string",
        "hasNextPage": true,
        "page": 1,
        "pageSize": 1,
        "results": [
          {
            "address1": "string",
            "city": "string",
            "country": "string",
            "entityType": "string",
            "lassoId": "string",
            "name": "Ava Chen",
            "postalCode": 1,
            "score": 1,
            "status": "string"
          }
        ],
        "resultsFound": 1,
        "resultsReturned": 1,
        "totalPages": 1
      },
      "people": {
        "results": [
          {
            "companies": [
              {
                "lassoId": "string",
                "name": "Ava Chen"
              }
            ],
            "entityType": "string",
            "lassoId": "string",
            "name": "Ava Chen",
            "score": 1,
            "totalCompanyCount": 1
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies.continuationToken` | string |  |
| `companies.hasNextPage` | boolean |  |
| `companies.page` | number |  |
| `companies.pageSize` | number |  |
| `companies.results[].address1` | string |  |
| `companies.results[].city` | string |  |
| `companies.results[].country` | string |  |
| `companies.results[].entityType` | string |  |
| `companies.results[].lassoId` | string |  |
| `companies.results[].name` | string |  |
| `companies.results[].postalCode` | number |  |
| `companies.results[].score` | number |  |
| `companies.results[].status` | string |  |
| `companies.resultsFound` | number |  |
| `companies.resultsReturned` | number |  |
| `companies.totalPages` | number |  |
| `people.results[].companies[].lassoId` | string |  |
| `people.results[].companies[].name` | string |  |
| `people.results[].entityType` | string |  |
| `people.results[].lassoId` | string |  |
| `people.results[].name` | string |  |
| `people.results[].score` | number |  |
| `people.results[].totalCompanyCount` | number |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /data/cvr/search` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-cvr.md) for the provider-specific parameters and requirements.

