# Datarobot: Get Use Case

Retrieves details for a use case from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-use-case
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-use-case?connectionId=$CONNECTION_ID&useCaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "useCaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/get-use-case?${params}`, {
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
| `useCaseId` | string | yes | The ID of the use case. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "datasetsCount": 1,
      "deploymentsCount": 1,
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectsCount": 1,
      "registeredModelsCount": 1,
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `datasetsCount` | number |  |
| `deploymentsCount` | number |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectsCount` | number |  |
| `registeredModelsCount` | number |  |
| `role` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /useCases/:useCaseId/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-use-case.md) for the provider-specific parameters and requirements.

