# FogBugz: List Milestones

Retrieves milestones from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-milestones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-milestones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-milestones?${params}`, {
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
| `ixProject` | number | no | Show milestones for a specific project. |
| `ixFixFor` | number | no | Include a specific milestone even if it is unassignable. |
| `fIncludeDeleted` | boolean | no | Set to true to include unassignable milestones. |
| `fIncludeReallyDeleted` | boolean | no | Set to true to include deleted milestones. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dt": "string",
      "dtStart": "string",
      "fDeleted": true,
      "fReallyDeleted": true,
      "ixFixFor": 1,
      "ixProject": 1,
      "setixFixForDependency": "string",
      "sFixFor": "string",
      "sProject": "string",
      "sStartNote": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dt` | string | Milestone due date. |
| `dtStart` | string | Milestone start date. |
| `fDeleted` | boolean | Whether the milestone is deleted. |
| `fReallyDeleted` | boolean | Whether the milestone is permanently deleted. |
| `ixFixFor` | number | Milestone ID. |
| `ixProject` | number | Project ID. |
| `setixFixForDependency` | string | Dependent milestone ID set. |
| `sFixFor` | string | Milestone name. |
| `sProject` | string | Project name. |
| `sStartNote` | string | Milestone start note. |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listFixFors` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-milestones.md) for the provider-specific parameters and requirements.

