# Zoho Tables: List Views

Retrieves all views from Zoho Tables.

```
GET https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-views?connectionId=$CONNECTION_ID&baseId=string&tableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseId": "string",
  "tableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/list-views?${params}`, {
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
| `baseId` | string | yes |  |
| `tableId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isActiveView": true,
      "isFilterApplied": true,
      "isSortApplied": true,
      "name": "Ava Chen",
      "type": "string",
      "viewId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isActiveView` | boolean | Whether this is the active view. |
| `isFilterApplied` | boolean | Whether filtering is applied to the view. |
| `isSortApplied` | boolean | Whether sorting is applied to the view. |
| `name` | string | View name. |
| `type` | string | Zoho view type code. |
| `viewId` | string | Zoho view identifier. |

## Native endpoint

Through the native Zoho Tables API, this operation is `GET /views` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-views.md) for the provider-specific parameters and requirements.

