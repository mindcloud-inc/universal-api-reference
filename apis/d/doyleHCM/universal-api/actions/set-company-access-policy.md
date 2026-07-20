# Doyle HCM: Set company access policy

Updates the company access policy in Doyle HCM.

```
PUT https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/set-company-access-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/set-company-access-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "allowEePortalForEes": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/set-company-access-policy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "allowEePortalForEes": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes |  |
| `allowEePortalForEes` | boolean | yes |  |

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
| `allowedApplicationsForEes` | number | Embedded employee-application access state after the update. |

## Native endpoint

Through the native Doyle HCM API, this operation is `POST /wep/companies/:companyId/access-policy` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-company-access-policy.md) for the provider-specific parameters and requirements.

