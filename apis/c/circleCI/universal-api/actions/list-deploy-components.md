# CircleCI: List Deploy Components



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-deploy-components
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-deploy-components?connectionId=$CONNECTION_ID&orgId=afbcafd1-31ea-4324-bc26-bf5d7e8e3e16&pageSize=20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "afbcafd1-31ea-4324-bc26-bf5d7e8e3e16",
  "pageSize": "20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-deploy-components?${params}`, {
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
| `orgId` | string | yes | The CircleCI organization UUID. Default: `afbcafd1-31ea-4324-bc26-bf5d7e8e3e16`. |
| `pageSize` | number | yes | Number of records to return. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "releaseCount": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `releaseCount` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /deploy/components` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deploy-components.md) for the provider-specific parameters and requirements.

