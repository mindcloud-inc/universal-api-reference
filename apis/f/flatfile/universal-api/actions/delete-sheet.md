# Flatfile: Delete Sheet

Deletes an existing sheet from Flatfile.

```
DELETE https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/delete-sheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/delete-sheet?connectionId=$CONNECTION_ID&sheetId=us_sht_mindcloud_flatfile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sheetId": "us_sht_mindcloud_flatfile"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/delete-sheet?${params}`, {
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
| `sheetId` | string | yes | Flatfile sheet ID. Default: `us_sht_mindcloud_flatfile`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the delete succeeded. |

## Native endpoint

Through the native Flatfile API, this operation is `DELETE /sheets/:sheetId` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sheet.md) for the provider-specific parameters and requirements.

