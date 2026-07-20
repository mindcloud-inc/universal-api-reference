# Quentn: List Contact Comments



```
GET https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quentn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-comments?connectionId=$CONNECTION_ID&contactId=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-comments?${params}`, {
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
| `contactId` | number | yes | Numeric Quentn contact id. Example: `123`. |
| `range` | number | no | Zero-based comment range offset. Default is 0. Example: `0`. |
| `limit` | number | no | Maximum number of comments to return. Default is 50 and upper limit is 50. Example: `50`. |
| `sort` | string | no | Sort order for the comments response. Example: `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "limit": 1,
      "numberComments": "string",
      "numberRanges": 1,
      "range": 1,
      "sort": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> | The list of Quentn comments for the contact. |
| `limit` | number | The page size returned by Quentn. |
| `numberComments` | string | The total number of comments available for the contact. |
| `numberRanges` | number | The total number of available ranges returned by Quentn. |
| `range` | number | The current pagination offset returned by Quentn. |
| `sort` | string | The sort direction applied by Quentn. |

## Native endpoint

Through the native Quentn API, this operation is `GET /contact/:contact_id/comments` (base URL `https://tbg6y3.us-1.quentn.com/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-comments.md) for the provider-specific parameters and requirements.

