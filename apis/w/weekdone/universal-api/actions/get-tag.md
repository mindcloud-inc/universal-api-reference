# Weekdone: Get Tag

Retrieves a specific tag from Weekdone.

```
GET https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weekdone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/get-tag?connectionId=$CONNECTION_ID&tagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/get-tag?${params}`, {
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
| `tagId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "tag": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `tag` | object |  |

## Native endpoint

Through the native Weekdone API, this operation is `GET tag/:tagId` (base URL `https://api.weekdone.com/1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

