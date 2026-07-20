# DatoCMS: Get Record



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record?connectionId=$CONNECTION_ID&itemId=LtUziyVcQpaAiV81ERJSMg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "LtUziyVcQpaAiV81ERJSMg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-record?${params}`, {
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
| `itemId` | string | yes | Example: `LtUziyVcQpaAiV81ERJSMg`. |
| `version` | string | no | Whether to return the currently published version (`published`) or latest available (`current`, default). Example: `current`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nested` | boolean | no | For Modular Content, Structured Text and Single Block fields. If set, returns full payload for nested blocks instead of IDs. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "meta": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Record attributes |
| `id` | string | Record ID |
| `meta` | object | Record state metadata |
| `relationships` | object | Linked resources |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /items/:itemId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

