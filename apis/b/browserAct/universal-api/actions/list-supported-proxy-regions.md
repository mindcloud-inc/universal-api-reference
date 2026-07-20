# BrowserAct: List Supported Proxy Regions

Retrieves supported proxy regions from BrowserAct.

```
GET https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-supported-proxy-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BrowserAct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-supported-proxy-regions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-supported-proxy-regions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | BrowserAct proxy region code. |
| `name` | string | Human-readable region name. |

## Native endpoint

Through the native BrowserAct API, this operation is `GET /get-region-list` (base URL `https://api.browseract.com/v2/workflow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-proxy-regions.md) for the provider-specific parameters and requirements.

