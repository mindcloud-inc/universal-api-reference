# DatoCMS: Delete Record



```
DELETE https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-record?connectionId=$CONNECTION_ID&itemId=LtUziyVcQpaAiV81ERJSMg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "LtUziyVcQpaAiV81ERJSMg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-record?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Deleted record ID |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `DELETE /items/:itemId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record.md) for the provider-specific parameters and requirements.

