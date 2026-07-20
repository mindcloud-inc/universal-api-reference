# Doyle HCM: List company positions

Retrieves company positions from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-positions?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-positions?${params}`, {
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
| `code` | string | Position code. |
| `id` | number | Position identifier. |
| `name` | string | Position name. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies/:companyId/positions` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-positions.md) for the provider-specific parameters and requirements.

