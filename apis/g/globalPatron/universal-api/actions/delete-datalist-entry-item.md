# Global Patron: Delete Datalist Entry Item

Deletes a datalist entry item from Global Patron.

```
DELETE https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-datalist-entry-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-datalist-entry-item?connectionId=$CONNECTION_ID&datalistId=string&datalistEntryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datalistId": "string",
  "datalistEntryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-datalist-entry-item?${params}`, {
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
| `datalistId` | string | yes | ID of the datalist. |
| `datalistEntryId` | string | yes | ID of the datalist entry item to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datalistEntryDeleted": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datalistEntryDeleted` | boolean | Whether the datalist entry item was deleted. |
| `message` | string | Provider status message. |

## Native endpoint

Through the native Global Patron API, this operation is `DELETE /api/restricted/datalist/{datalistId}/entry/{datalistEntryId}` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-datalist-entry-item.md) for the provider-specific parameters and requirements.

