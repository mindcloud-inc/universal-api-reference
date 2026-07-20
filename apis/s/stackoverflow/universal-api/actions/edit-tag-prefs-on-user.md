# Stackoverflow: Edit Tag Preferences

Updates a user's tag preferences in Stackoverflow.

```
PUT https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/edit-tag-prefs-on-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/edit-tag-prefs-on-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/edit-tag-prefs-on-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "is_favorite": true,
      "is_ignored": true,
      "tag_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_favorite` | boolean |  |
| `is_ignored` | boolean |  |
| `tag_name` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `POST /users/[:id]/tag-preferences/edit` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-tag-prefs-on-user.md) for the provider-specific parameters and requirements.

