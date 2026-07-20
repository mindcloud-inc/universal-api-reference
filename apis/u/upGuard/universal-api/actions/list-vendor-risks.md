# UpGuard: List Vendor Risks

Retrieves active risks for a vendor in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-risks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-risks?connectionId=$CONNECTION_ID&primaryHostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "primaryHostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-vendor-risks?${params}`, {
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
| `primaryHostname` | string | yes | The primary hostname of the vendor to return risks for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "risks": [
        {
          "category": "string",
          "description": "string",
          "finding": "string",
          "firstDetected": "string",
          "hostnameCount": 1,
          "hostnames": [
            "Ava Chen"
          ],
          "id": "string",
          "remediation": "string",
          "risk": "string",
          "riskSubtype": "string",
          "riskType": "string",
          "severity": "string"
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
| `risks[].category` | string |  |
| `risks[].description` | string |  |
| `risks[].finding` | string |  |
| `risks[].firstDetected` | string |  |
| `risks[].hostnameCount` | number |  |
| `risks[].hostnames[]` | string |  |
| `risks[].id` | string |  |
| `risks[].remediation` | string |  |
| `risks[].risk` | string |  |
| `risks[].riskSubtype` | string |  |
| `risks[].riskType` | string |  |
| `risks[].severity` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /risks/vendors` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendor-risks.md) for the provider-specific parameters and requirements.

