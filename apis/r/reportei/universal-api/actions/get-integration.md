# Reportei: Get Integration

Retrieves an integration from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-integration?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-integration?${params}`, {
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
| `id` | number | yes | ID da integração. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "integration": {
        "id": 1,
        "name": "Ava Chen",
        "project_id": 1,
        "slug": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `integration.id` | number | Integration identifier |
| `integration.name` | string | Integration name |
| `integration.project_id` | number | Project identifier |
| `integration.slug` | string | Integration slug |
| `integration.status` | string | Integration status |

## Native endpoint

Through the native Reportei API, this operation is `GET /integrations/:id` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration.md) for the provider-specific parameters and requirements.

