# SureContact: Get Reports Overview

Retrieves high-level reporting metrics from SureContact.

```
GET https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/get-reports-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/get-reports-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/get-reports-overview?${params}`, {
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
| `compareEndDate` | string | no |  |
| `compareStartDate` | string | no |  |
| `compareWith` | string | no |  |
| `dateRange` | string | no |  |
| `endDate` | string | no |  |
| `groupBy` | string | no |  |
| `startDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comparison_period": {},
      "contacts": {},
      "emails": {},
      "engagement": {},
      "period": {},
      "revenue": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comparison_period` | object |  |
| `contacts` | object |  |
| `emails` | object |  |
| `engagement` | object |  |
| `period` | object |  |
| `revenue` | object |  |

## Native endpoint

Through the native SureContact API, this operation is `GET api/v1/public/reports/overview` (base URL `https://api.surecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reports-overview.md) for the provider-specific parameters and requirements.

