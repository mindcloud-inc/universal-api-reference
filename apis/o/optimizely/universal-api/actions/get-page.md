# Optimizely: Get Page

Retrieves page details from the Optimizely API.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-page?connectionId=$CONNECTION_ID&pageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-page?${params}`, {
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
| `pageId` | string | yes | The page id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activationType": "string",
      "archived": true,
      "created": "string",
      "editUrl": "https://example.com",
      "id": 1,
      "key": "string",
      "lastModified": "string",
      "name": "Ava Chen",
      "pageType": "string",
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activationType` | string |  |
| `archived` | boolean |  |
| `created` | string |  |
| `editUrl` | string |  |
| `id` | number |  |
| `key` | string |  |
| `lastModified` | string |  |
| `name` | string |  |
| `pageType` | string |  |
| `projectId` | number |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /pages/{pageId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page.md) for the provider-specific parameters and requirements.

