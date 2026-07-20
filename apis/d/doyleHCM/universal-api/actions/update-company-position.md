# Doyle HCM: Update company position

Updates a company position in Doyle HCM.

```
PUT https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/update-company-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/update-company-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "positionId": 1,
  "name": "Ava Chen",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/update-company-position', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "positionId": 1,
    "name": "Ava Chen",
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes |  |
| `positionId` | number | yes |  |
| `name` | string | yes |  |
| `code` | string | yes |  |
| `defaultRate` | number | no |  |
| `defaultWCCode` | string | no |  |
| `rate` | object | no |  |
| `annualSalary` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Updated position code. |
| `id` | number | Updated position identifier. |
| `name` | string | Updated position name. |

## Native endpoint

Through the native Doyle HCM API, this operation is `PATCH /wep/companies/:companyId/positions/:positionId` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company-position.md) for the provider-specific parameters and requirements.

