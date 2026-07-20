# DMSales: Delete Contact Note

Deletes an existing contact note from DMSales.

```
DELETE https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/delete-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/delete-contact-note?connectionId=$CONNECTION_ID&baseKey=string&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseKey": "string",
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/delete-contact-note?${params}`, {
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
| `baseKey` | string | yes | Contact base key. |
| `noteId` | string | yes | Note UUID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native DMSales API, this operation is `DELETE /api/contact-card/delete-note` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-note.md) for the provider-specific parameters and requirements.

