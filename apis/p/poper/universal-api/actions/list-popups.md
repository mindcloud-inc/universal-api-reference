# Poper: List Popups

Retrieves all popups from your Poper account.

```
GET https://connect.mindcloud.co/v1/universal/poper/latest/actions/list-popups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poper/latest/actions/list-popups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poper/latest/actions/list-popups?${params}`, {
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
      "popups": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `popups` | array<object> | Array of popups returned for the authenticated Poper account. |

## Native endpoint

Through the native Poper API, this operation is `POST /popup/list` (base URL `https://api.poper.ai/general/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-popups.md) for the provider-specific parameters and requirements.

