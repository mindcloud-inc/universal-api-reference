# Doyle HCM: List company departments

Retrieves company departments from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-departments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-departments?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-departments?${params}`, {
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
| `id` | number | Department identifier. |
| `name` | string | Department name. |
| `phone` | string | Department phone number when returned. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies/:companyId/departments` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-departments.md) for the provider-specific parameters and requirements.

