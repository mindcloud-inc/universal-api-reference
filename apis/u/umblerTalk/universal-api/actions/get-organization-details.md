# Umbler Talk: Get Organization Details

Retrieves organization details from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization-details?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization-details?${params}`, {
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
| `id` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "cnpj": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "financeEmail": "ava@example.com",
      "iconUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "phone": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `cnpj` | string |  |
| `createdAtUTC` | date |  |
| `financeEmail` | string |  |
| `iconUrl` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/organizations/[:id]/details/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-details.md) for the provider-specific parameters and requirements.

