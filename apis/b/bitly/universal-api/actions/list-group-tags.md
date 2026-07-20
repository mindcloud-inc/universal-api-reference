# Bitly: List Group Tags

Retrieves tags for a group in Bitly.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-tags?connectionId=$CONNECTION_ID&groupGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/list-group-tags?${params}`, {
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
| `groupGuid` | string | yes | The Bitly group GUID. |
| `type` | string | no | Filter tags by resource type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags[]` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /groups/:group_guid/tags` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-tags.md) for the provider-specific parameters and requirements.

