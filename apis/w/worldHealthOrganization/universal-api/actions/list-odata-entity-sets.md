# World Health Organization: List OData Entity Sets

Retrieves OData entity sets from the World Health Organization.

```
GET https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-odata-entity-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World Health Organization `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-odata-entity-sets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-odata-entity-sets?${params}`, {
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
      "kind": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `kind` | string |  |
| `name` | string |  |
| `url` | string |  |

## Native endpoint

Through the native World Health Organization API, this operation is `GET /` (base URL `https://ghoapi.azureedge.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-odata-entity-sets.md) for the provider-specific parameters and requirements.

