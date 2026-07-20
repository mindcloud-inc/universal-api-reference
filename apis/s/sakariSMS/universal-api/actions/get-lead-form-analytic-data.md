# Sakari SMS: Get Lead Form Analytic Data

Retrieves lead form analytics from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-lead-form-analytic-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-lead-form-analytic-data?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-lead-form-analytic-data?${params}`, {
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
| `formId` | string | yes |  |
| `start` | string | no | General search term that specifies start date |
| `end` | string | no | General search term that specifies end date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversions": 1,
      "data": {
        "data": [
          {
            "conversions": 1,
            "date": "string",
            "impressions": 1
          }
        ]
      },
      "impressions": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversions` | number |  |
| `data` | array<object> |  |
| `data.data[].conversions` | number |  |
| `data.data[].date` | string |  |
| `data.data[].impressions` | number |  |
| `impressions` | number |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/forms/:formId/analytics` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-form-analytic-data.md) for the provider-specific parameters and requirements.

