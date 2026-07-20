# Prospeo: Get Job Title Suggestions

Finds job title suggestions in Prospeo.

```
GET https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/get-job-title-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prospeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/get-job-title-suggestions?connectionId=$CONNECTION_ID&jobTitleSearch=software%20engineer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobTitleSearch": "software engineer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/get-job-title-suggestions?${params}`, {
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
| `jobTitleSearch` | string | yes | Search query to find job title suggestions. Minimum 2 characters. Default: `software engineer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "jobTitleSuggestions": [
        "string"
      ],
      "locationSuggestions": [
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
| `error` | boolean |  |
| `jobTitleSuggestions` | array<string> |  |
| `locationSuggestions` | array<object> |  |

## Native endpoint

Through the native Prospeo API, this operation is `POST /search-suggestions` (base URL `https://api.prospeo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job-title-suggestions.md) for the provider-specific parameters and requirements.

