# Scale: Get Multiple Projects



```
GET https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-multiple-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-multiple-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scale/latest/actions/get-multiple-projects?${params}`, {
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
| `createdAfter` | string | no | Only return projects created after this ISO 8601 timestamp. |
| `createdBefore` | string | no | Only return projects created before this ISO 8601 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projects": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projects` | array<object> | Array of project objects. |

## Native endpoint

Through the native Scale API, this operation is `GET /v2/projects` (base URL `https://api.scale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-multiple-projects.md) for the provider-specific parameters and requirements.

