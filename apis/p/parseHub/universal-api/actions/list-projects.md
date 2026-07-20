# ParseHub: List Projects



```
GET https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ParseHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/list-projects?${params}`, {
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
| `limit` | number | no | Number of projects to return. ParseHub accepts values from 1 through 20. Default: `20`. |
| `offset` | number | no | Zero-based offset into the project list. Default: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeOptions` | number | no | Set to 1 to include project options and webhook metadata in each result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projects": [
        {
          "lastReadyRun": {
            "runToken": "string"
          },
          "lastRun": {
            "runToken": "string"
          },
          "mainSite": "string",
          "mainTemplate": "string",
          "optionsJson": "string",
          "title": "string",
          "token": "string"
        }
      ],
      "totalProjects": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projects` | array<object> | Projects in the current ParseHub account page. |
| `projects[].lastReadyRun.runToken` | string |  |
| `projects[].lastRun.runToken` | string |  |
| `projects[].mainSite` | string |  |
| `projects[].mainTemplate` | string |  |
| `projects[].optionsJson` | string |  |
| `projects[].title` | string |  |
| `projects[].token` | string |  |
| `totalProjects` | number | Total number of projects in the account. |

## Native endpoint

Through the native ParseHub API, this operation is `GET /projects` (base URL `https://www.parsehub.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

