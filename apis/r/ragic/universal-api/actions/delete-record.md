# Ragic: Delete Record

Deletes an existing record from Ragic.

```
DELETE https://connect.mindcloud.co/v1/universal/ragic/latest/actions/delete-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/delete-record?connectionId=$CONNECTION_ID&tabFolderPath=ragic-setup&sheetIndex=8&recordId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "8",
  "recordId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ragic/latest/actions/delete-record?${params}`, {
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
| `tabFolderPath` | string | yes | The folder path from the Ragic URL, for example `ragic-setup`. Default: `ragic-setup`. |
| `sheetIndex` | number | yes | The sheet number from the Ragic URL. Default: `8`. |
| `recordId` | number | yes | The record ID from the Ragic record URL. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "msg": "string",
      "ragicId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `msg` | string | Deletion result message from Ragic. |
| `ragicId` | number | The Ragic record ID affected by the delete request. |

## Native endpoint

Through the native Ragic API, this operation is `DELETE /:tabFolderPath/:sheetIndex/:recordId` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-record.md) for the provider-specific parameters and requirements.

