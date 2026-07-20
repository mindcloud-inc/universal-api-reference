# Rebrandly: Get Tag Details

Retrieves details for a tag in Rebrandly.

```
GET https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-tag-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rebrandly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-tag-details?connectionId=$CONNECTION_ID&id=cfa87d9986144793b8608026ef7aa50e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "cfa87d9986144793b8608026ef7aa50e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rebrandly/latest/actions/get-tag-details?${params}`, {
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
| `id` | string | yes | Unique identifier of the tag. Example: `cfa87d9986144793b8608026ef7aa50e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "clicks": 1,
      "color": "string",
      "id": "string",
      "name": "Ava Chen",
      "scans": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `clicks` | number |  |
| `color` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scans` | object |  |

## Native endpoint

Through the native Rebrandly API, this operation is `GET /tags/:id` (base URL `https://api.rebrandly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag-details.md) for the provider-specific parameters and requirements.

