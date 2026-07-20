# CircleCI: Get Organization



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-organization?connectionId=$CONNECTION_ID&orgSlugOrId=circleci%2FNheMuBArzQftQimV3Bqqky" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgSlugOrId": "circleci/NheMuBArzQftQimV3Bqqky"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-organization?${params}`, {
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
| `orgSlugOrId` | string | yes | The CircleCI organization slug or ID. Default: `circleci/NheMuBArzQftQimV3Bqqky`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "slug": "string",
      "vcsType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `vcsType` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /organization/:org_slug_or_id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

