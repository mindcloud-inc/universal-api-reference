# Morningmate: Search SSO Participating Projects

Retrieves Morningmate SSO projects for a participant.

```
GET https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-sso-participating-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morningmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-sso-participating-projects?connectionId=$CONNECTION_ID&participantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "participantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-sso-participating-projects?${params}`, {
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
| `participantId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projectId": "string",
      "projectUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectId` | string | Project ID. |
| `projectUrl` | string | SSO project URL. |
| `title` | string | Project title. |

## Native endpoint

Through the native Morningmate API, this operation is `GET /v1/sso/projects/participants/[:participantId]` (base URL `https://api.morningmate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sso-participating-projects.md) for the provider-specific parameters and requirements.

