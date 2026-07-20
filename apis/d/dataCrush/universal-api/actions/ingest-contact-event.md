# DataCrush: Search Contacts By Contact Key

Finds contacts in DataCrush by contact key.

```
GET https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/ingest-contact-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataCrush `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/ingest-contact-event?connectionId=$CONNECTION_ID&contact_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataCrush/latest/actions/ingest-contact-event?${params}`, {
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
| `contact_key` | string | yes | Unique contact key to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "rows": [
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
| `result` | string |  |
| `rows` | array<object> |  |

## Native endpoint

Through the native DataCrush API, this operation is `POST /contact/search` (base URL `https://api.datacrush.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ingest-contact-event.md) for the provider-specific parameters and requirements.

