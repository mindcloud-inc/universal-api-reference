# CircleCI: Get Project Environment Variable



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-environment-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-environment-variable?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-project-environment-variable?${params}`, {
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
| `name` | string | no | Environment variable name. |
| `projectSlug` | string | no | Project slug in the form vcs/org/repo. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `value` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /project/:project_slug/envvar/:name` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-environment-variable.md) for the provider-specific parameters and requirements.

