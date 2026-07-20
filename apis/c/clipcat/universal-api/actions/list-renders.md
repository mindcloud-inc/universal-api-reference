# Clipcat: List Renders

Retrieves video renders for the current Clipcat workspace.

```
GET https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/list-renders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clipcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/list-renders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clipcat/latest/actions/list-renders?${params}`, {
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
| `completed` | boolean | no | Set to true to return only completed renders. |
| `page` | number | no | The page number of render results to retrieve. |
| `template` | string | no | Filter renders by template UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "credits": 1,
      "metadata": "string",
      "modifications": [
        {}
      ],
      "progress": 1,
      "self": "string",
      "status": "string",
      "template": "string",
      "uid": "string",
      "url": "https://example.com",
      "webhook_response_code": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `credits` | number |  |
| `metadata` | string |  |
| `modifications` | array<object> |  |
| `progress` | number |  |
| `self` | string |  |
| `status` | string |  |
| `template` | string |  |
| `uid` | string |  |
| `url` | string |  |
| `webhook_response_code` | number |  |
| `webhook_url` | string |  |

## Native endpoint

Through the native Clipcat API, this operation is `GET /v1/renders` (base URL `https://api.clipcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-renders.md) for the provider-specific parameters and requirements.

