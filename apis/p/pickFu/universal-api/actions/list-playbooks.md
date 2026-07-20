# PickFu: List Playbooks



```
GET https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-playbooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-playbooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/list-playbooks?${params}`, {
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
| `industry` | string | no | Filter playbooks by industry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "duration": "string",
      "icon": "string",
      "industry": "string",
      "name": "Ava Chen",
      "poll_count": 1,
      "slug": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Short description of the playbook. |
| `duration` | string | Estimated completion time. |
| `icon` | string | Icon identifier or emoji. |
| `industry` | string | Industry category. |
| `name` | string | Playbook name. |
| `poll_count` | number | Number of polls in the playbook. |
| `slug` | string | Unique playbook identifier. |
| `url` | string | Direct PickFu URL for the playbook. |

## Native endpoint

Through the native PickFu API, this operation is `GET /playbooks` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-playbooks.md) for the provider-specific parameters and requirements.

