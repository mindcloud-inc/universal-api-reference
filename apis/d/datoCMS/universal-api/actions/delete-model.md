# DatoCMS: Delete Model



```
DELETE https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-model?connectionId=$CONNECTION_ID&itemTypeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemTypeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/delete-model?${params}`, {
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
| `itemTypeId` | string | yes | Model ID or API key. |

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
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `DELETE /item-types/:itemTypeId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-model.md) for the provider-specific parameters and requirements.

