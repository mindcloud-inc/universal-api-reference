# Doyle HCM: Update company department

Updates a company department in Doyle HCM.

```
PUT https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/update-company-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/update-company-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "departmentId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/update-company-department', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "departmentId": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes |  |
| `departmentId` | number | yes |  |
| `name` | string | yes |  |
| `phone` | string | no |  |
| `ext` | string | no |  |
| `managerId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Updated department identifier. |
| `name` | string | Updated department name. |
| `phone` | string | Updated department phone number when returned. |

## Native endpoint

Through the native Doyle HCM API, this operation is `PATCH /wep/companies/:companyId/departments/:departmentId` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company-department.md) for the provider-specific parameters and requirements.

