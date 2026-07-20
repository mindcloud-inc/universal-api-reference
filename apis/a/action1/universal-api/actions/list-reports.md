# Action1: List Reports

Retrieves all enterprise reports from Action1.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-reports?${params}`, {
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
| `subtree` | list | no | Specify if you want to query the entire report subtree. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": "string",
      "description": "string",
      "id": "string",
      "largeImage": "string",
      "longDescription": "string",
      "name": "Ava Chen",
      "parentCategory": "string",
      "self": "string",
      "smallImage": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | string |  |
| `description` | string |  |
| `id` | string |  |
| `largeImage` | string |  |
| `longDescription` | string |  |
| `name` | string |  |
| `parentCategory` | string |  |
| `self` | string |  |
| `smallImage` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /reports/all` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

