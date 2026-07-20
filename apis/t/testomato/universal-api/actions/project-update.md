# Testomato: Project update

Updates an existing project in Testomato.

```
PUT https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testomato/latest/actions/project-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `url` | string | no |  |
| `title` | string | no |  |
| `period` | string | no |  |
| `timeout` | number | no |  |
| `delay` | number | no |  |
| `sslAlertPeriod` | number | no |  |
| `checkDefaultErrors` | boolean | no |  |
| `uptimeEnabled` | number | no |  |
| `uptimeUrl` | string | no |  |
| `userAgent` | string | no |  |

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

Through the native Testomato API, this operation is `PUT /project/:id` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/project-update.md) for the provider-specific parameters and requirements.

