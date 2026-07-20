# Neon: List shared projects

Retrieves shared projects from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-shared-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-shared-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-shared-projects?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no | Neon API parameter search |
| `timeout` | number | no | Neon API parameter timeout |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "projects": [
        {}
      ],
      "unavailable_project_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `projects` | array<object> |  |
| `unavailable_project_ids` | array<string> |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects/shared` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shared-projects.md) for the provider-specific parameters and requirements.

