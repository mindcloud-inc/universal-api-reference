# Neon: List projects

Retrieves projects from Neon.

```
GET https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Neon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neon/latest/actions/list-projects?${params}`, {
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
| `org_id` | string | no | Neon API parameter org_id |
| `timeout` | number | no | Neon API parameter timeout |
| `recoverable` | boolean | no | Neon API parameter recoverable |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applications": {},
      "integrations": {},
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
| `applications` | object |  |
| `integrations` | object |  |
| `pagination` | object |  |
| `projects` | array<object> |  |
| `unavailable_project_ids` | array<string> |  |

## Native endpoint

Through the native Neon API, this operation is `GET /projects` (base URL `https://console.neon.tech/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

