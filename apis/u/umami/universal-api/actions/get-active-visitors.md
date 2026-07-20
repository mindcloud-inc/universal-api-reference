# Umami: Get Active Visitors



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-active-visitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-active-visitors?connectionId=$CONNECTION_ID&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-active-visitors?${params}`, {
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
| `websiteId` | string | yes | The website ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "visitors": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `visitors` | number | Unique active visitors in the last five minutes. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/active` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-active-visitors.md) for the provider-specific parameters and requirements.

