# WellTraq: Get Form Analytics Fields

Retrieves form analytics fields from WellTraq.

```
GET https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-form-analytics-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WellTraq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-form-analytics-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-form-analytics-fields?${params}`, {
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
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "fieldName": "Ava Chen",
      "fieldValue": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `effectiveDate` | date |  |
| `fieldName` | string |  |
| `fieldValue` | string |  |

## Native endpoint

Through the native WellTraq API, this operation is `GET /Forms/GetAnalyticsFields` (base URL `https://welltraq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-analytics-fields.md) for the provider-specific parameters and requirements.

