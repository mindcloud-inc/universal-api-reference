# Algolia: Search Multiple Indices

Searches multiple Algolia indices in one request.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-multiple-indices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-multiple-indices?connectionId=$CONNECTION_ID&requests%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requests[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/search-multiple-indices?${params}`, {
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
| `requests[]` | array<object> | yes | Search requests to run across one or more indices. |
| `strategy` | list | no | Whether to run all queries or stop after enough matches. One of: `0`, `1`. Default: `none`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/*/queries` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-multiple-indices.md) for the provider-specific parameters and requirements.

