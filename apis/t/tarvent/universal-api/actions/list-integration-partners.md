# Tarvent: List Integration Partners

Retrieves integration partners from Tarvent.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-integration-partners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-integration-partners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-integration-partners?${params}`, {
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
      "authType": 1,
      "dscr": "string",
      "helpUrl": "https://example.com",
      "id": "string",
      "integrationCategory": "string",
      "isConfigurable": true,
      "isEmbed": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authType` | number |  |
| `dscr` | string |  |
| `helpUrl` | string |  |
| `id` | string |  |
| `integrationCategory` | string |  |
| `isConfigurable` | boolean |  |
| `isEmbed` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-integration-partners.md) for the provider-specific parameters and requirements.

