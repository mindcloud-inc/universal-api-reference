# Crowdin: Download Project Translations

Retrieves a download link for project translations in Crowdin.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/download-project-translations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/download-project-translations?connectionId=$CONNECTION_ID&projectId=1&buildId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "buildId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/download-project-translations?${params}`, {
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
| `projectId` | number | yes |  |
| `buildId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expireIn": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expireIn` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /projects/:projectId/translations/builds/:buildId/download` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-project-translations.md) for the provider-specific parameters and requirements.

