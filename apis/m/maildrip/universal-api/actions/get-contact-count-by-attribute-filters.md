# Maildrip: Get contact count by attribute filters



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contact-count-by-attribute-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contact-count-by-attribute-filters?connectionId=$CONNECTION_ID&attributeFilters=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attributeFilters": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-contact-count-by-attribute-filters?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributeFilters` | string | yes | JSON array of filter objects. Format: [{"key":"plan","operator":"equals","value":"pro"}] |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/contacts/count` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-count-by-attribute-filters.md) for the provider-specific parameters and requirements.

