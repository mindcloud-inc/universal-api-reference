# MoreApp: Schedule Export

Schedules a submission export in MoreApp.

```
POST https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/schedule-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoreApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/schedule-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "formId": "string",
  "exporterType": "string",
  "mailOnFinish[]": [
    "string"
  ],
  "submissionIds[]": [
    "string"
  ],
  "options.timezone": "string",
  "options.languageCode": "string",
  "exportFields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/schedule-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "formId": "string",
    "exporterType": "string",
    "mailOnFinish[]": ["string"],
    "submissionIds[]": ["string"],
    "options.timezone": "string",
    "options.languageCode": "string",
    "exportFields[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes |  |
| `formId` | string | yes |  |
| `exporterType` | string | yes |  |
| `mailOnFinish[]` | array<string> | yes |  |
| `submissionIds[]` | array<string> | yes |  |
| `options.timezone` | string | yes |  |
| `options.languageCode` | string | yes |  |
| `exportFields[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Export job identifier returned by MoreApp. |

## Native endpoint

Through the native MoreApp API, this operation is `POST /api/v1.0/customers/{{customerId}}/forms/{{formId}}/submissions/export` (base URL `https://api.moreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-export.md) for the provider-specific parameters and requirements.

