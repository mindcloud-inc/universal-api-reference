# UpGuard: Get Portfolio Risk Profile Overview

Retrieves a portfolio risk overview from UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-portfolio-risk-profile-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-portfolio-risk-profile-overview?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-portfolio-risk-profile-overview?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "risks": [
        {
          "categoryTitle": "string",
          "dateFirstDetected": "string",
          "description": "string",
          "factCategory": "string",
          "id": "string",
          "numFailedVendors": 1,
          "riskType": "string",
          "severity": "string",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string |  |
| `risks[].categoryTitle` | string |  |
| `risks[].dateFirstDetected` | string |  |
| `risks[].description` | string |  |
| `risks[].factCategory` | string |  |
| `risks[].id` | string |  |
| `risks[].numFailedVendors` | number |  |
| `risks[].riskType` | string |  |
| `risks[].severity` | string |  |
| `risks[].title` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /risks/vendors/all` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-portfolio-risk-profile-overview.md) for the provider-specific parameters and requirements.

