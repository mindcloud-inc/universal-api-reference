# Cirra: List Connections

Retrieves Cirra connections for the authenticated user.

```
GET https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cirra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-connections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-connections?${params}`, {
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
| `appId` | string | no | Optional app ID to filter connections by app. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeWorkflowCount": 1,
      "app": {
        "id": "string",
        "name": "Ava Chen",
        "slug": "string"
      },
      "attemptedOn": "2026-05-07T12:00:00.000Z",
      "authenticatedOn": "2026-05-07T12:00:00.000Z",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "credentialId": "string",
      "id": "string",
      "isDefault": true,
      "label": "string",
      "status": "string",
      "statusAsOf": "2026-05-07T12:00:00.000Z",
      "testedOn": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "workflowCount": 1,
      "workflowStepCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeWorkflowCount` | number |  |
| `app.id` | string |  |
| `app.name` | string |  |
| `app.slug` | string |  |
| `attemptedOn` | date |  |
| `authenticatedOn` | date |  |
| `createdOn` | date |  |
| `credentialId` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `label` | string |  |
| `status` | string |  |
| `statusAsOf` | date |  |
| `testedOn` | date |  |
| `type` | string |  |
| `updatedOn` | date |  |
| `workflowCount` | number |  |
| `workflowStepCount` | number |  |

## Native endpoint

Through the native Cirra API, this operation is `GET /v1/cirra/connections` (base URL `http://api-public:9801`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connections.md) for the provider-specific parameters and requirements.

