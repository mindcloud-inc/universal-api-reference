# Uspacy: List CRM Entities

Retrieves available CRM entity types from Uspacy.

```
GET https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-crm-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-crm-entities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-crm-entities?${params}`, {
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
      "data": [
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
| `data` | array<object> |  |

## Native endpoint

Through the native Uspacy API, this operation is `GET /crm/v1/entity` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-crm-entities.md) for the provider-specific parameters and requirements.

