# fynk: List Document Metadata Values

Retrieves metadata values for a document in fynk.

```
GET https://connect.mindcloud.co/v1/universal/fynk/latest/actions/list-document-metadata-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/list-document-metadata-values?connectionId=$CONNECTION_ID&document=25c718b2-be8b-44e7-858f-3152e7380022" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document": "25c718b2-be8b-44e7-858f-3152e7380022"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fynk/latest/actions/list-document-metadata-values?${params}`, {
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
| `document` | string | yes | The document UUID. Default: `25c718b2-be8b-44e7-858f-3152e7380022`. |

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

Through the native fynk API, this operation is `GET /documents/:document/metadata-values` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-metadata-values.md) for the provider-specific parameters and requirements.

