# GrowthBook: Find a single sdk connection by its key

Retrieves an SDK connection by key from GrowthBook.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/lookup-sdk-connection-by-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/lookup-sdk-connection-by-key?connectionId=$CONNECTION_ID&key=my-first-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "my-first-project"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/lookup-sdk-connection-by-key?${params}`, {
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
| `key` | string | yes | The key of the requested sdkConnection Default: `my-first-project`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sdkConnection": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sdkConnection` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /sdk-connections/lookup/:key` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-sdk-connection-by-key.md) for the provider-specific parameters and requirements.

