# NextLead: Identify Organization

Verifies your API key and retrieves your NextLead organization.

```
GET https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/identify-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/identify-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/identify-organization?${params}`, {
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |

## Native endpoint

Through the native NextLead API, this operation is `GET /api/v2/identify-user` (base URL `https://dashboard.nextlead.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-organization.md) for the provider-specific parameters and requirements.

