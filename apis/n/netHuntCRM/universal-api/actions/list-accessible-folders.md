# NetHunt CRM: List Accessible Folders

Retrieves accessible folders from NetHunt CRM.

```
GET https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/list-accessible-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetHunt CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/list-accessible-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/list-accessible-folders?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native NetHunt CRM API, this operation is `GET /triggers/readable-folder` (base URL `https://nethunt.com/api/v1/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accessible-folders.md) for the provider-specific parameters and requirements.

