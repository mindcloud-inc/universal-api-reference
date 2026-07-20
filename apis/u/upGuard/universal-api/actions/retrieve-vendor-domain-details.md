# UpGuard: Retrieve Vendor Domain Details

Retrieves details for a vendor domain in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-vendor-domain-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-vendor-domain-details?connectionId=$CONNECTION_ID&vendorPrimaryHostname=Ava%20Chen&hostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vendorPrimaryHostname": "Ava Chen",
  "hostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-vendor-domain-details?${params}`, {
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
| `vendorPrimaryHostname` | string | yes | The primary hostname of the vendor to show the domain detail for. |
| `hostname` | string | yes | The domain hostname for which to return details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automatedScore": 1,
      "checkResults": [
        {
          "actual": [
            {
              "property": "string",
              "value": "string"
            }
          ],
          "category": "string",
          "checkedAt": "string",
          "description": "string",
          "expected": [
            {
              "property": "string",
              "value": "string"
            }
          ],
          "id": "string",
          "pass": true,
          "riskSubtype": "string",
          "riskType": "string",
          "severity": 1,
          "severityName": "Ava Chen",
          "title": "string"
        }
      ],
      "hostname": "Ava Chen",
      "scannedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automatedScore` | number |  |
| `checkResults[].actual[].property` | string |  |
| `checkResults[].actual[].value` | string |  |
| `checkResults[].category` | string |  |
| `checkResults[].checkedAt` | string |  |
| `checkResults[].description` | string |  |
| `checkResults[].expected[].property` | string |  |
| `checkResults[].expected[].value` | string |  |
| `checkResults[].id` | string |  |
| `checkResults[].pass` | boolean |  |
| `checkResults[].riskSubtype` | string |  |
| `checkResults[].riskType` | string |  |
| `checkResults[].severity` | number |  |
| `checkResults[].severityName` | string |  |
| `checkResults[].title` | string |  |
| `hostname` | string |  |
| `scannedAt` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /vendor/domain` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-vendor-domain-details.md) for the provider-specific parameters and requirements.

