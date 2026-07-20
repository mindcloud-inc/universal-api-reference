# SWELLEnterprise: Create Company

Creates a new company in SWELLEnterprise.

```
POST https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The company name. |
| `email` | string | no | The company email. |
| `phone` | string | no | The company phone. |
| `website` | string | no | The company website. |
| `address` | string | no | The company address. |
| `notes` | string | no | Notes about the company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "address": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "deletedAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "enrichedAt": "2026-05-07T12:00:00.000Z",
        "enrichedData": {},
        "id": 1,
        "name": "Ava Chen",
        "notes": [
          "string"
        ],
        "phone": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "website": "string"
      },
      "message": "string",
      "meta": {
        "timestamp": "2026-05-07T12:00:00.000Z",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.address` | string | The company address. |
| `data.createdAt` | date | When the company was created. |
| `data.deletedAt` | date | When the company was deleted. |
| `data.email` | string | The company email. |
| `data.enrichedAt` | date | When the company was enriched. |
| `data.enrichedData` | object | Enriched company data. |
| `data.id` | number | The company ID. |
| `data.name` | string | The company name. |
| `data.notes` | array<string> | Notes about the company. |
| `data.phone` | string | The company phone. |
| `data.updatedAt` | date | When the company was last updated. |
| `data.website` | string | The company website. |
| `message` | string | Success message. |
| `meta.timestamp` | date | Response timestamp. |
| `meta.version` | string | API version. |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /crm/companies` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

