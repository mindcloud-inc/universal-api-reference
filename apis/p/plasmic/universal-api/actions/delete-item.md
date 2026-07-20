# Plasmic: Delete Item

Deletes an item from Plasmic CMS.

```
DELETE https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/delete-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plasmic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/delete-item?connectionId=$CONNECTION_ID&rowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plasmic/latest/actions/delete-item?${params}`, {
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
| `rowId` | string | yes | The Plasmic row identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "rowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the row delete completed successfully. |
| `rowId` | string | The deleted Plasmic CMS row ID from the request. |

## Native endpoint

Through the native Plasmic API, this operation is `DELETE /rows/:rowId` (base URL `https://data.plasmic.app/api/v1/cms`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-item.md) for the provider-specific parameters and requirements.

