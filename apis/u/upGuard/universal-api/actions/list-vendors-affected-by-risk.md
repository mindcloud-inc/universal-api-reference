# UpGuard: List Vendors Affected By Risk

Retrieves vendors affected by a risk in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendors-affected-by-risk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendors-affected-by-risk?connectionId=$CONNECTION_ID&riskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "riskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendors-affected-by-risk?${params}`, {
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
| `riskId` | string | yes | The risk ID to filter by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "riskId": "string",
      "riskSeverity": "string",
      "riskType": "string",
      "totalVendorsMatchingFilter": 1,
      "vendorsWithRisk": [
        {
          "countHostnamesFailed": 1,
          "dateDetected": "string",
          "isPartiallyWaived": true,
          "isWaived": true,
          "name": "Ava Chen",
          "primaryHostname": "Ava Chen",
          "score": 1,
          "vendorId": 1
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
| `riskId` | string |  |
| `riskSeverity` | string |  |
| `riskType` | string |  |
| `totalVendorsMatchingFilter` | number |  |
| `vendorsWithRisk[].countHostnamesFailed` | number |  |
| `vendorsWithRisk[].dateDetected` | string |  |
| `vendorsWithRisk[].isPartiallyWaived` | boolean |  |
| `vendorsWithRisk[].isWaived` | boolean |  |
| `vendorsWithRisk[].name` | string |  |
| `vendorsWithRisk[].primaryHostname` | string |  |
| `vendorsWithRisk[].score` | number |  |
| `vendorsWithRisk[].vendorId` | number |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /risks/vendors_with_risk` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendors-affected-by-risk.md) for the provider-specific parameters and requirements.

