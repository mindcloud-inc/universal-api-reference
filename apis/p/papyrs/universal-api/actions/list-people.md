# Papyrs: List People



```
GET https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-people?${params}`, {
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
      "attributes": {},
      "avatar_large": "string",
      "distinguished_name": "Ava Chen",
      "id": "string",
      "role_id": "string",
      "subgroup_id": "string",
      "waiting_invite": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Directory attributes keyed by attribute label. |
| `avatar_large` | string | Avatar image URL. |
| `distinguished_name` | string | Directory distinguished name. |
| `id` | string | Papyrs user ID. |
| `role_id` | string | Papyrs role identifier. |
| `subgroup_id` | string | Papyrs subgroup ID. |
| `waiting_invite` | boolean | Whether the user is still waiting on their invite. |

## Native endpoint

Through the native Papyrs API, this operation is `GET /people/all/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

