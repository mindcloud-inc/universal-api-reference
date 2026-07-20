# Testomato: New project

Creates a new project in Testomato.

```
POST https://connect.mindcloud.co/v1/universal/testomato/latest/actions/new-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/new-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testomato/latest/actions/new-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes |  |
| `addPresetChecks` | boolean | no |  |

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

Through the native Testomato API, this operation is `POST /project/create` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/new-project.md) for the provider-specific parameters and requirements.

