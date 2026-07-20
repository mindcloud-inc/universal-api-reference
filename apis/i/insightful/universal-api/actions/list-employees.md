# Insightful: List Employees

Retrieves employees from your Insightful account.

```
GET https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-employees?${params}`, {
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
| `select` | string | no | Comma-separated employee fields to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deactivated": 1,
      "email": "ava@example.com",
      "id": "string",
      "identifier": "string",
      "invited": 1,
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "pseudonymId": 1,
      "sharedSettingsId": "string",
      "teamId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deactivated` | number |  |
| `email` | string |  |
| `id` | string |  |
| `identifier` | string |  |
| `invited` | number |  |
| `modelName` | string |  |
| `name` | string |  |
| `pseudonymId` | number |  |
| `sharedSettingsId` | string |  |
| `teamId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Insightful API, this operation is `GET /employee` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

