# CircleCI: List URL Orb Allow List Entries



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-url-orb-allow-list-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-url-orb-allow-list-entries?connectionId=$CONNECTION_ID&orgSlugOrId=circleci%2FNheMuBArzQftQimV3Bqqky" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgSlugOrId": "circleci/NheMuBArzQftQimV3Bqqky"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/list-url-orb-allow-list-entries?${params}`, {
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
      "auth": "string",
      "id": "string",
      "name": "Ava Chen",
      "prefix": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | string |  |
| `id` | string |  |
| `name` | string |  |
| `prefix` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /organization/:org_slug_or_id/url-orb-allow-list` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-url-orb-allow-list-entries.md) for the provider-specific parameters and requirements.

