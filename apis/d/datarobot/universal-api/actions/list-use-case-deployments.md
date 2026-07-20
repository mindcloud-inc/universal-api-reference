# Datarobot: List Use Case Deployments

Retrieves deployments for a use case from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-case-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-case-deployments?connectionId=$CONNECTION_ID&useCaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "useCaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-use-case-deployments?${params}`, {
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
      "description": "string",
      "id": "string",
      "label": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userHasAccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `label` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userHasAccess` | boolean |  |

## Native endpoint

Through the native Datarobot API, this operation is `GET /useCases/:useCaseId/deployments/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-use-case-deployments.md) for the provider-specific parameters and requirements.

