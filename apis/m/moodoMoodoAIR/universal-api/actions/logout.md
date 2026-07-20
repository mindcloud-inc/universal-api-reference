# Moodo & Moodo AIR: Logout

Signs the current user out of Moodo.

```
DELETE https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/logout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/logout?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/logout?${params}`, {
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
      "accepted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted` | boolean |  |

## Native endpoint

Through the native Moodo & Moodo AIR API, this operation is `POST /logout` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/logout.md) for the provider-specific parameters and requirements.

