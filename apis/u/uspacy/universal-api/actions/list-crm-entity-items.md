# Uspacy: List CRM Entity Items

Retrieves CRM entity items from Uspacy.

```
GET https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-crm-entity-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-crm-entity-items?connectionId=$CONNECTION_ID&entity=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entity": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/list-crm-entity-items?${params}`, {
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
| `entity` | string | yes | The CRM entity key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `links` | object |  |
| `meta` | object |  |

## Native endpoint

Through the native Uspacy API, this operation is `GET /crm/v1/entities/:entity` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-crm-entity-items.md) for the provider-specific parameters and requirements.

