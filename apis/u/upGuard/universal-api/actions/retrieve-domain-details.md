# UpGuard: Retrieve Domain Details

Retrieves details for a domain in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-domain-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-domain-details?connectionId=$CONNECTION_ID&hostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-domain-details?${params}`, {
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
| `hostname` | string | yes | The hostname for which to return the details, e.g. "upguard.com" |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aRecords": [
        "string"
      ],
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
          "sources": [
            "string"
          ],
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
| `aRecords[]` | string |  |
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
| `checkResults[].sources[]` | string |  |
| `checkResults[].title` | string |  |
| `hostname` | string |  |
| `scannedAt` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /domain` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-domain-details.md) for the provider-specific parameters and requirements.

