# Statsig: Get Company Info

Retrieves company info from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-company-info-get-console-v1-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-company-info-get-console-v1-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-company-info-get-console-v1-company?${params}`, {
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
      "companyID": "string",
      "companyName": "Ava Chen",
      "isWarehouseNative": true,
      "orgID": "string",
      "orgName": "Ava Chen",
      "resultsUpTo": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyID` | string | Statsig company/project identifier. |
| `companyName` | string | Statsig company name. |
| `isWarehouseNative` | boolean | Whether the company is warehouse native. |
| `orgID` | string | Statsig organization identifier, when present. |
| `orgName` | string | Statsig organization name, when present. |
| `resultsUpTo` | number | Latest available results timestamp. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/company` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-info-get-console-v1-company.md) for the provider-specific parameters and requirements.

