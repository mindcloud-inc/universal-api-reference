# Quantum Digital: Check Dashboard Access



```
GET https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/check-dashboard-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/check-dashboard-access?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/check-dashboard-access?${params}`, {
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
      "currentUrl": "https://example.com",
      "errorMsg": "string",
      "html": "string",
      "redirectToTop": true,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentUrl` | string | Current URL for the verification flow. |
| `errorMsg` | string | Error message returned by the provider. |
| `html` | string | HTML returned by the provider. |
| `redirectToTop` | boolean | Whether the provider requested a top-level redirect. |
| `success` | boolean | Whether dashboard access was verified successfully. |

## Native endpoint

Through the native Quantum Digital API, this operation is `POST /devplatform/checkdashboardaccess` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-dashboard-access.md) for the provider-specific parameters and requirements.

