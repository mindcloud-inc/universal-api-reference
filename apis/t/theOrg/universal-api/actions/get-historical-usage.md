# The Org: Get Historical Usage

Retrieves historical API usage from The Org.

```
GET https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-historical-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-historical-usage?connectionId=$CONNECTION_ID&api=0&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "api": "0",
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-historical-usage?${params}`, {
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
| `api` | list | yes | The The Org API family to inspect in usage history. One of: `0`, `1`, `2`. |
| `from` | string | yes | Start date in YYYY-MM-DD format |
| `to` | string | yes | End date in YYYY-MM-DD format |
| `interval` | list | no | The aggregation interval for the returned stats. One of: `0`, `1`. Default: `daily`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "api": "string",
        "stats": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.api` | string | The historical usage endpoint identifier requested |
| `data.stats` | array<object> | Historical usage buckets returned by The Org |

## Native endpoint

Through the native The Org API, this operation is `GET /v1.1/usage/history` (base URL `https://api.theorg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-usage.md) for the provider-specific parameters and requirements.

