# SparkPost: Retrieve Account



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-account?${params}`, {
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
| `include` | string | no | Optional include value. Set to `usage` to include account usage data. Example: `usage`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anniversaryDate": "2026-05-07T12:00:00.000Z",
      "companyName": "Ava Chen",
      "countryCode": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "options": {},
      "serviceLevel": "string",
      "status": "string",
      "statusReasonCategory": "string",
      "statusUpdated": "2026-05-07T12:00:00.000Z",
      "subscription": {},
      "tfaRequired": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anniversaryDate` | date | Billing anniversary date. |
| `companyName` | string | Account company name. |
| `countryCode` | string | Two-letter country code for the account. |
| `created` | date | Account creation timestamp. |
| `customerId` | number | SparkPost account identifier. |
| `options` | object | Account-level SparkPost options. |
| `serviceLevel` | string | SparkPost service level. |
| `status` | string | Current account status. |
| `statusReasonCategory` | string | Status reason category when present. |
| `statusUpdated` | date | Timestamp when status was last updated. |
| `subscription` | object | Current SparkPost subscription details. |
| `tfaRequired` | boolean | Whether two-factor authentication is required. |
| `updated` | date | Last account update timestamp. |

## Native endpoint

Through the native SparkPost API, this operation is `GET /account` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-account.md) for the provider-specific parameters and requirements.

