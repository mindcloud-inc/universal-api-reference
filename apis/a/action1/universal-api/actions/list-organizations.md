# Action1: List Organizations

Retrieves organizations from the current Action1 enterprise.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-organizations?${params}`, {
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
| `admin` | string | no | Specify 'yes' to get all organizations where the current user is at least an organization admin. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "enterpriseId": "string",
      "id": "string",
      "name": "Ava Chen",
      "self": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `enterpriseId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /organizations` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

