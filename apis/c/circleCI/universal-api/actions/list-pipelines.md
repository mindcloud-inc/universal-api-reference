# CircleCI: List Pipelines



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-pipelines?connectionId=$CONNECTION_ID&orgSlug=circleci%2FNheMuBArzQftQimV3Bqqky" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgSlug": "circleci/NheMuBArzQftQimV3Bqqky"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-pipelines?${params}`, {
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
| `orgSlug` | string | yes | Organization slug in the form vcs-slug/org-name. Default: `circleci/NheMuBArzQftQimV3Bqqky`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "number": 1,
      "projectSlug": "string",
      "state": "string",
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
| `number` | number |  |
| `projectSlug` | string |  |
| `state` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /pipeline` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.

