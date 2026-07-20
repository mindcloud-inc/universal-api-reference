# Raven Tools: List Keywords

Retrieves keywords for a domain in Raven Tools.

```
GET https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-keywords?connectionId=$CONNECTION_ID&domain=mindcloud.co" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "mindcloud.co"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/list-keywords?${params}`, {
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
| `domain` | string | yes | The domain to inspect for configured keywords. Default: `mindcloud.co`. Example: `mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | A keyword configured for the domain. |

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-keywords.md) for the provider-specific parameters and requirements.

