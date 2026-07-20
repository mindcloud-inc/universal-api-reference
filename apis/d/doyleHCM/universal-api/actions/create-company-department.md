# Doyle HCM: Create company department

Creates a company department in Doyle HCM.

```
POST https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/create-company-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/create-company-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/create-company-department', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
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
| `id` | number | Created department identifier. |
| `name` | string | Created department name. |
| `phone` | string | Created department phone number when returned. |

## Native endpoint

Through the native Doyle HCM API, this operation is `POST /wep/companies/:companyId/departments` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company-department.md) for the provider-specific parameters and requirements.

