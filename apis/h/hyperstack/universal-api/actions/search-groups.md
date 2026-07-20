# Hyperstack Certificates: Search Groups



```
GET https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/search-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/search-groups?connectionId=$CONNECTION_ID&page=1&page_size=50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page": "1",
  "page_size": "50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/search-groups?${params}`, {
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
| `keyword` | string | no | Search keyword matched against group titles. |
| `title` | string | no | Alias for keyword when filtering by group title. |
| `strict` | boolean | no | When true, require a contiguous phrase match. |
| `page` | number | yes | The page number for pagination. Default: `1`. |
| `page_size` | number | yes | The number of groups to return per page. Default: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "groupCode": "string",
      "groupKey": "string",
      "lastModified": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | ISO timestamp when the group was created. |
| `groupCode` | string | Credential group code. |
| `groupKey` | string | Credential group identifier. |
| `lastModified` | string | ISO timestamp when the group was last modified. |
| `title` | string | Credential group title. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /groups/search` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-groups.md) for the provider-specific parameters and requirements.

