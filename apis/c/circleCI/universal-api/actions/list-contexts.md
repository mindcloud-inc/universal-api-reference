# CircleCI: List Contexts



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-contexts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-contexts?connectionId=$CONNECTION_ID&ownerId=afbcafd1-31ea-4324-bc26-bf5d7e8e3e16" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ownerId": "afbcafd1-31ea-4324-bc26-bf5d7e8e3e16"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-contexts?${params}`, {
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
| `ownerId` | string | yes | The CircleCI organization ID. Default: `afbcafd1-31ea-4324-bc26-bf5d7e8e3e16`. |
| `ownerType` | string | no | The CircleCI owner type. Use organization for cloud orgs. Default: `organization`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen"
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

## Native endpoint

Through the native CircleCI API, this operation is `GET /context` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contexts.md) for the provider-specific parameters and requirements.

