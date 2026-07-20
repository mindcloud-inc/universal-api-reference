# Insightful: Get Employee

Retrieves an employee from your Insightful account.

```
GET https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-employee?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-employee?${params}`, {
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
| `id` | string | yes | The employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deactivated": 1,
      "email": "ava@example.com",
      "id": "string",
      "identifier": "string",
      "invited": 1,
      "localDataRetention": 1,
      "logLevel": "string",
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "pseudonymId": 1,
      "sharedSettingsId": "string",
      "teamId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdAt` | date |  |
| `deactivated` | number |  |
| `email` | string |  |
| `id` | string |  |
| `identifier` | string |  |
| `invited` | number |  |
| `localDataRetention` | number |  |
| `logLevel` | string |  |
| `modelName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `pseudonymId` | number |  |
| `sharedSettingsId` | string |  |
| `teamId` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Insightful API, this operation is `GET /employee/:id` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

