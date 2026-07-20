# YouGile: Get column

Retrieves details for a column from YouGile.

```
GET https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-column
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouGile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-column?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youGile/latest/actions/get-column?${params}`, {
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
| `id` | string | yes | The YouGile column ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boardId": "string",
      "color": 1,
      "deleted": true,
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boardId` | string |  |
| `color` | number |  |
| `deleted` | boolean |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native YouGile API, this operation is `GET /columns/:id` (base URL `{{credentials.companyDomain}}/api-v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-column.md) for the provider-specific parameters and requirements.

