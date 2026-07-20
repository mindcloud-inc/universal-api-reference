# Global Patron: Delete Datalist

Deletes a datalist from Global Patron.

```
DELETE https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-datalist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-datalist?connectionId=$CONNECTION_ID&datalistId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datalistId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/delete-datalist?${params}`, {
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
| `datalistId` | string | yes | ID of the datalist to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionSuccessful": true,
      "error": "string",
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionSuccessful` | boolean | Whether GlobalPatron reports the delete was successful. |
| `error` | string | Provider error message when present. |
| `id` | string | Deleted datalist identifier. |
| `message` | string | Provider status message. |

## Native endpoint

Through the native Global Patron API, this operation is `POST /api/restricted/datalist/{datalistId}?for_deletion=1` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-datalist.md) for the provider-specific parameters and requirements.

