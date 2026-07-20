# GitScrum: Get Project Stats

Retrieves statistics for a specific GitScrum project.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-project-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-project-stats?connectionId=$CONNECTION_ID&companySlug=string&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companySlug": "string",
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-project-stats?${params}`, {
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
| `companySlug` | string | yes |  |
| `slug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tasks": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tasks` | object |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /projects/:slug/stats` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-stats.md) for the provider-specific parameters and requirements.

