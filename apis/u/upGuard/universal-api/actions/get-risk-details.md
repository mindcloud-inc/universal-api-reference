# UpGuard: Get Risk Details

Retrieves details for an UpGuard risk.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-risk-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-risk-details?connectionId=$CONNECTION_ID&riskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "riskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/get-risk-details?${params}`, {
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
| `riskId` | string | yes | ID of the risk to fetch details for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "description": "string",
      "finding": "string",
      "generic": true,
      "group": "string",
      "id": "string",
      "remediation": "string",
      "risk": "string",
      "riskDetails": "string",
      "riskSubtype": "string",
      "riskType": "string",
      "severity": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `description` | string |  |
| `finding` | string |  |
| `generic` | boolean |  |
| `group` | string |  |
| `id` | string |  |
| `remediation` | string |  |
| `risk` | string |  |
| `riskDetails` | string |  |
| `riskSubtype` | string |  |
| `riskType` | string |  |
| `severity` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /available_risks/risk` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-risk-details.md) for the provider-specific parameters and requirements.

