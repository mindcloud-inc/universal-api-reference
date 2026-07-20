# Lasso X: List Company Delta

Retrieves changed companies from Lasso X since a given date.

```
GET https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-company-delta
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lasso X `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-company-delta?connectionId=$CONNECTION_ID&since=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "since": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lassoX/latest/actions/list-company-delta?${params}`, {
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
| `since` | date | yes | Start date for delta search, e.g. 2021-02-01. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `max` | date | no | Maximum date for delta search. |
| `page_size` | number | no | Number of results to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "continuationToken": "string",
      "hasNextPage": true,
      "page": 1,
      "pageSize": 1,
      "results": [
        {
          "address": {
            "address1": "string",
            "postalCode": 1
          },
          "cvr": 1,
          "form": {
            "code": 1
          },
          "industry": {
            "text": "string"
          },
          "lassoId": "string",
          "lastStatusChange": "2026-05-07T12:00:00.000Z",
          "lastUpdated": "2026-05-07T12:00:00.000Z",
          "lifeTime": {
            "from": "2026-05-07T12:00:00.000Z"
          },
          "name": "Ava Chen",
          "status": "string",
          "unitNumber": 1
        }
      ],
      "resultsFound": 1,
      "resultsReturned": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `continuationToken` | string |  |
| `hasNextPage` | boolean |  |
| `page` | number |  |
| `pageSize` | number |  |
| `results[].address.address1` | string |  |
| `results[].address.postalCode` | number |  |
| `results[].cvr` | number |  |
| `results[].form.code` | number |  |
| `results[].industry.text` | string |  |
| `results[].lassoId` | string |  |
| `results[].lastStatusChange` | date |  |
| `results[].lastUpdated` | date |  |
| `results[].lifeTime.from` | date |  |
| `results[].name` | string |  |
| `results[].status` | string |  |
| `results[].unitNumber` | number |  |
| `resultsFound` | number |  |
| `resultsReturned` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Lasso X API, this operation is `GET /data/cvr/company/delta` (base URL `https://api.lassox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-delta.md) for the provider-specific parameters and requirements.

