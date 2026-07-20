# Vybit: List Vybits (Legacy OAuth)



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-vybits-legacy-oauth
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-vybits-legacy-oauth?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-vybits-legacy-oauth?${params}`, {
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
      "name": "Ava Chen",
      "triggerKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Display name of the vybit. |
| `triggerKey` | string | Legacy trigger key for the vybit. |

## Native endpoint

Through the native Vybit API, this operation is `GET /rest/vybit_list` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vybits-legacy-oauth.md) for the provider-specific parameters and requirements.

