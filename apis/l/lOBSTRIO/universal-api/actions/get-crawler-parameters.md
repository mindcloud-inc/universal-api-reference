# LOBSTR.IO: Get Crawler Parameters

Retrieves crawler parameters from LOBSTR.IO.

```
GET https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-crawler-parameters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-crawler-parameters?connectionId=$CONNECTION_ID&crawlerHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlerHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/get-crawler-parameters?${params}`, {
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
| `crawlerHash` | string | yes | The unique identifier (hash) of the crawler. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "squid": {},
      "task": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `squid` | object |  |
| `task` | object |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `GET /v1/crawlers/:crawler_hash/params` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawler-parameters.md) for the provider-specific parameters and requirements.

