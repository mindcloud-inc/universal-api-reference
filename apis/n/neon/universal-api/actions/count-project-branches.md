# Neon: Retrieve number of branches

Retrieves the number of branches from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/count-project-branches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/count-project-branches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/count-project-branches?${params}`, {
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
| `project_id` | string | no | Neon API parameter project_id |
| `search` | string | no | Count branches matching the name in the search query |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branches_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branches_count` | number |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/:project_id/branches/count` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-project-branches.md) for the provider-specific parameters and requirements.

