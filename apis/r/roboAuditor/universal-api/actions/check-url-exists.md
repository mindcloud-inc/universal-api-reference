# RoboAuditor: Check URL Exists



```
GET https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/check-url-exists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RoboAuditor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/check-url-exists?connectionId=$CONNECTION_ID&websiteUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roboAuditor/latest/actions/check-url-exists?${params}`, {
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
| `websiteUrl` | string | yes | Website URL to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exist": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exist` | string | Raw upstream HTTP response summary returned by provider endpoint. |

## Native endpoint

Through the native RoboAuditor API, this operation is `GET /urlExist` (base URL `https://app.siteauditor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-url-exists.md) for the provider-specific parameters and requirements.

