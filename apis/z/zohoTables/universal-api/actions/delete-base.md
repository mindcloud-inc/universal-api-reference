# Zoho Tables: Delete Base

Deletes an existing base from Zoho Tables.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/delete-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/delete-base?connectionId=$CONNECTION_ID&portalId=1&baseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "1",
  "baseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/delete-base?${params}`, {
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
| `portalId` | number | yes |  |
| `baseId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseId` | string | Zoho base identifier. |

## Native endpoint

Through the native Zoho Tables API, this operation is `DELETE /bases` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-base.md) for the provider-specific parameters and requirements.

