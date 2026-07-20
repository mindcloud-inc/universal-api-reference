# Doyle HCM: Get company access policy

Retrieves the company access policy from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-access-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-access-policy?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company-access-policy?${params}`, {
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
      "allowedApplicationsForEes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedApplicationsForEes` | number | Embedded employee-application access state for the company. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies/:companyId/access-policy` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-access-policy.md) for the provider-specific parameters and requirements.

