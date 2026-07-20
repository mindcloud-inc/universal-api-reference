# DMSales: Get Refer Score Report ID

Retrieves a Refer Score report ID from DMSales.

```
GET https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-refer-score-report-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-refer-score-report-id?connectionId=$CONNECTION_ID&nip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-refer-score-report-id?${params}`, {
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
| `nip` | string | yes | Polish tax identification number for report lookup. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "details": "string",
      "exception_type": "string",
      "message": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `details` | string |  |
| `exception_type` | string |  |
| `message` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native DMSales API, this operation is `GET /api/person/get-refer-score-report-id` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-refer-score-report-id.md) for the provider-specific parameters and requirements.

