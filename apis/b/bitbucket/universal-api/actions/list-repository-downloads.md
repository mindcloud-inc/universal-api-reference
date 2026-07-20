# Bitbucket: List Repository Downloads

Retrieves repository download artifacts from Bitbucket.

```
GET https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/list-repository-downloads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitbucket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/list-repository-downloads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/list-repository-downloads?${params}`, {
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
      "next": "string",
      "page": 1,
      "pagelen": 1,
      "previous": "string",
      "size": 1,
      "values": [
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
| `next` | string |  |
| `page` | number |  |
| `pagelen` | number |  |
| `previous` | string |  |
| `size` | number |  |
| `values` | array<object> |  |

## Native endpoint

Through the native Bitbucket API, this operation is `GET /repositories/:workspace/:repo_slug/downloads` (base URL `https://api.bitbucket.org/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-repository-downloads.md) for the provider-specific parameters and requirements.

