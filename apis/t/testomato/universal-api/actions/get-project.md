# Testomato: Get project

Retrieves a project from Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/get-project?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkDefaultErrors": true,
      "created": "string",
      "delay": 1,
      "id": "string",
      "location": "string",
      "payerId": 1,
      "period": "string",
      "permissions": {},
      "sslAlertPeriod": 1,
      "sslDaysLeft": 1,
      "sslExpiration": "string",
      "sslStatus": "string",
      "timeout": 1,
      "title": "string",
      "uptimeEnabled": 1,
      "uptimeUrl": "https://example.com",
      "url": "https://example.com",
      "userIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkDefaultErrors` | boolean |  |
| `created` | string |  |
| `delay` | number |  |
| `id` | string |  |
| `location` | string |  |
| `payerId` | number |  |
| `period` | string |  |
| `permissions` | object |  |
| `sslAlertPeriod` | number |  |
| `sslDaysLeft` | number |  |
| `sslExpiration` | string |  |
| `sslStatus` | string |  |
| `timeout` | number |  |
| `title` | string |  |
| `uptimeEnabled` | number |  |
| `uptimeUrl` | string |  |
| `url` | string |  |
| `userIds` | array<number> |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:id` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

