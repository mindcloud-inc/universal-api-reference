# Stackoverflow: Get Site Info

Retrieves specific site information from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-site-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-site-info?connectionId=$CONNECTION_ID&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-site-info?${params}`, {
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
| `site` | string | yes | API site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_revision": "string",
      "total_answers": 1,
      "total_badges": 1,
      "total_comments": 1,
      "total_questions": 1,
      "total_users": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_revision` | string |  |
| `total_answers` | number |  |
| `total_badges` | number |  |
| `total_comments` | number |  |
| `total_questions` | number |  |
| `total_users` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /info` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-info.md) for the provider-specific parameters and requirements.

