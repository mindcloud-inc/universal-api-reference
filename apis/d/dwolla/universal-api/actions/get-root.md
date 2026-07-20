# Dwolla: Get Root

Retrieves the API root for accessible Dwolla resources.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-root
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-root?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-root?${params}`, {
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
      "_links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for the Dwolla API root. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-root.md) for the provider-specific parameters and requirements.

