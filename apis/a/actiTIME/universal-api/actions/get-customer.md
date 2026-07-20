# actiTIME: Get Customer

Retrieves a specific customer from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-customer?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-customer?${params}`, {
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
| `id` | number | yes | Customer identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedActions": {
        "canDelete": true,
        "canModify": true
      },
      "archived": true,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedActions.canDelete` | boolean | Whether the customer can be deleted. |
| `allowedActions.canModify` | boolean | Whether the customer can be modified. |
| `archived` | boolean | Whether the customer is archived. |
| `created` | date | Creation date and time. |
| `description` | string | Customer description. |
| `id` | number | Unique customer identifier. |
| `name` | string | Customer name. |
| `url` | string | Customer URL. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /customers/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

