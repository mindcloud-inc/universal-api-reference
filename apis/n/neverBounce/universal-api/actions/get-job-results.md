# NeverBounce: Get Job Results

Retrieves detailed job results from NeverBounce.

```
GET https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-job-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-job-results?connectionId=$CONNECTION_ID&jobId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/get-job-results?${params}`, {
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
| `jobId` | number | yes | NeverBounce job identifier. |
| `page` | number | no | Results page to retrieve. |
| `itemsPerPage` | number | no | Number of results to return per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": 1,
      "query": {
        "catchalls": 1,
        "disposables": 1,
        "invalids": 1,
        "itemsPerPage": 1,
        "jobId": 1,
        "page": 1,
        "unknowns": 1,
        "valids": 1
      },
      "results": [
        {
          "data": {
            "email": "ava@example.com",
            "name": "Ava Chen"
          },
          "verification": {
            "addressInfo": {
              "addr": "string",
              "alias": "string",
              "domain": "string",
              "fqdn": "string",
              "host": "string",
              "normalizedEmail": "ava@example.com",
              "originalEmail": "ava@example.com",
              "subdomain": "string",
              "tld": "string"
            },
            "flags": [
              "string"
            ],
            "result": "string",
            "suggestedCorrection": "string"
          }
        }
      ],
      "status": "string",
      "totalPages": 1,
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | number |  |
| `query` | object |  |
| `query.catchalls` | number |  |
| `query.disposables` | number |  |
| `query.invalids` | number |  |
| `query.itemsPerPage` | number |  |
| `query.jobId` | number |  |
| `query.page` | number |  |
| `query.unknowns` | number |  |
| `query.valids` | number |  |
| `results` | array<object> |  |
| `results[].data` | object |  |
| `results[].data.email` | string |  |
| `results[].data.name` | string |  |
| `results[].verification` | object |  |
| `results[].verification.addressInfo` | object |  |
| `results[].verification.addressInfo.addr` | string |  |
| `results[].verification.addressInfo.alias` | string |  |
| `results[].verification.addressInfo.domain` | string |  |
| `results[].verification.addressInfo.fqdn` | string |  |
| `results[].verification.addressInfo.host` | string |  |
| `results[].verification.addressInfo.normalizedEmail` | string |  |
| `results[].verification.addressInfo.originalEmail` | string |  |
| `results[].verification.addressInfo.subdomain` | string |  |
| `results[].verification.addressInfo.tld` | string |  |
| `results[].verification.flags` | array<string> |  |
| `results[].verification.result` | string |  |
| `results[].verification.suggestedCorrection` | string |  |
| `status` | string |  |
| `totalPages` | number |  |
| `totalResults` | number |  |

## Native endpoint

Through the native NeverBounce API, this operation is `GET /jobs/results` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-results.md) for the provider-specific parameters and requirements.

