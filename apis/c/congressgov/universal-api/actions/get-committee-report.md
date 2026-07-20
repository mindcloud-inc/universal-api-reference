# Congress.gov: Get Committee Report

Retrieves a committee report from Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-committee-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-committee-report?connectionId=$CONNECTION_ID&congress=118&reportType=hrpt&reportNumber=617" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "congress": "118",
  "reportType": "hrpt",
  "reportNumber": "617"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/get-committee-report?${params}`, {
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
| `congress` | number | yes | The congress number. For example, 118. Example: `118`. |
| `reportType` | string | yes | The committee report type. Values include hrpt, srpt, or erpt. Example: `hrpt`. |
| `reportNumber` | number | yes | The committee report's assigned number. For example, 617. Example: `617`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "committeeReports": [
        {}
      ],
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `committeeReports` | array<object> |  |
| `request` | object |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /committee-report/:congress/:reportType/:reportNumber` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-committee-report.md) for the provider-specific parameters and requirements.

