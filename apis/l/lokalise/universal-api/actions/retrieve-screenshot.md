# Lokalise: Retrieve Screenshot

Retrieves a screenshot from a Lokalise project.

```
GET https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/retrieve-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/retrieve-screenshot?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/retrieve-screenshot?${params}`, {
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
| `project_id` | string | no | Lokalise project identifier. |
| `screenshot_id` | string | no | Lokalise screenshot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "project_id": "string",
      "project_uuid": "string",
      "screenshot": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `project_id` | string |  |
| `project_uuid` | string |  |
| `screenshot` | object |  |

## Native endpoint

Through the native Lokalise API, this operation is `GET /projects/:project_id/screenshots/:screenshot_id` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-screenshot.md) for the provider-specific parameters and requirements.

