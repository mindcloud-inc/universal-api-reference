# Zapier NLA: Get Configuration Link



```
GET https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/get-configuration-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zapier NLA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/get-configuration-link?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/get-configuration-link?${params}`, {
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
      "configuration_link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration_link` | string |  |

## Native endpoint

Through the native Zapier NLA API, this operation is `GET /api/v1/configuration-link/` (base URL `https://actions.zapier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-configuration-link.md) for the provider-specific parameters and requirements.

