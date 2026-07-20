# Hyperstack Certificates: List All Groups



```
GET https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/list-all-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/list-all-groups?connectionId=$CONNECTION_ID&page=1&page_size=50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page": "1",
  "page_size": "50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/list-all-groups?${params}`, {
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
| `page` | number | yes | The page number for pagination. Default: `1`. |
| `page_size` | number | yes | The number of groups to return per page. Default: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "groupCode": "string",
      "groupId": "string",
      "title": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Credential group description HTML. |
| `groupCode` | string | Credential group code. |
| `groupId` | string | Credential group identifier. |
| `title` | string | Credential group title. |
| `website` | string | Credential group website URL. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `POST /groups/all` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-groups.md) for the provider-specific parameters and requirements.

