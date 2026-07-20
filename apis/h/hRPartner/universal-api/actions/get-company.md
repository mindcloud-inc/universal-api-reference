# HR Partner: Get Company



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-company?${params}`, {
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
| `customFields` | boolean | no | Include all employee custom fields in the company response. |
| `activeModules` | boolean | no | Include the list of active HR Partner modules in the company response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeEmployees": 1,
      "aiMonthlyApplicantLimit": 1,
      "employeeLimit": 1,
      "logoImageLink": "https://example.com",
      "name": "Ava Chen",
      "slug": "string",
      "smsCredits": 1,
      "subdomain": "string",
      "subscribed": true,
      "subscribedUntil": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "totalEmployees": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeEmployees` | number | Active employee count. |
| `aiMonthlyApplicantLimit` | number | Monthly AI applicant limit. |
| `employeeLimit` | number | Configured employee limit. |
| `logoImageLink` | string | Company logo image URL. |
| `name` | string | Company name. |
| `slug` | string | Company slug. |
| `smsCredits` | number | Remaining SMS credits. |
| `subdomain` | string | HR Partner subdomain. |
| `subscribed` | boolean | Whether the company is subscribed. |
| `subscribedUntil` | date | Subscription expiry timestamp. |
| `timezone` | string | Company timezone. |
| `totalEmployees` | number | Total employee count. |

## Native endpoint

Through the native HR Partner API, this operation is `GET /company` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

