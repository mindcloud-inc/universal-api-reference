# Callbell: List Custom Statuses

Retrieves custom statuses for the current Callbell account.

```
GET https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-custom-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callbell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-custom-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callbell/latest/actions/list-custom-statuses?${params}`, {
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
      "createdAt": "string",
      "emoji": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `emoji` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Callbell API, this operation is `GET /custom_statuses` (base URL `https://api.callbell.eu/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-statuses.md) for the provider-specific parameters and requirements.

