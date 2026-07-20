# Doyle HCM: Get company dashboard

Retrieves a company dashboard definition from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-dashboard?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-dashboard?${params}`, {
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
| `companyId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocked": true,
      "companyId": 1,
      "items": [
        {}
      ],
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean | Whether the company is blocked. |
| `companyId` | number | Company identifier for the dashboard payload. |
| `items` | array<object> | Dashboard widgets returned for the company. |
| `type` | number | Company dashboard payload type identifier. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies/:companyId/dashboard` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-dashboard.md) for the provider-specific parameters and requirements.

