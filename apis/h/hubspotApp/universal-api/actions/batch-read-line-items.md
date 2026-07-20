# HubSpot: Batch Read Line Items

Retrieves line items from HubSpot in a batch.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-line-items?connectionId=$CONNECTION_ID&inputs%5B%5D=%5Bobject%20Object%5D&inputs%5B%5D.id=79962112746" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputs[]": "[object Object]",
  "inputs[].id": "79962112746"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/batch-read-line-items?${params}`, {
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
| `inputs[]` | array<object> | yes | The line items to batch read. |
| `inputs[].id` | string | yes | The line item ID to batch read. Example: `79962112746`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties[]` | array<string> | no | Properties to include in each returned line item. |
| `propertiesWithHistory[]` | array<string> | no | Properties to include with history values in each returned line item. |
| `idProperty` | string | no | The unique property to use instead of the default record ID. Example: `hs_object_id`. |
| `archived` | boolean | no | Whether to read archived line items. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HubSpot API returns.

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/line_items/batch/read` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-read-line-items.md) for the provider-specific parameters and requirements.

