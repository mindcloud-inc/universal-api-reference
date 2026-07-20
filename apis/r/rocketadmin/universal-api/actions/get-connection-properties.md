# Rocketadmin: Get Connection Properties



```
GET https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-connection-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-connection-properties?connectionId=$CONNECTION_ID&connectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-connection-properties?${params}`, {
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
| `connectionId` | string | yes | Rocketadmin connection identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_ai_requests": true,
      "company_name": "Ava Chen",
      "default_showing_table": "string",
      "hidden_tables": [
        "string"
      ],
      "human_readable_table_names": true,
      "id": "string",
      "logo_url": "https://example.com",
      "primary_color": "string",
      "secondary_color": "string",
      "tables_audit": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_ai_requests` | boolean |  |
| `company_name` | string |  |
| `default_showing_table` | string |  |
| `hidden_tables` | array<string> |  |
| `human_readable_table_names` | boolean |  |
| `id` | string |  |
| `logo_url` | string |  |
| `primary_color` | string |  |
| `secondary_color` | string |  |
| `tables_audit` | boolean |  |

## Native endpoint

Through the native Rocketadmin API, this operation is `GET /connection/properties/:connectionId` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection-properties.md) for the provider-specific parameters and requirements.

