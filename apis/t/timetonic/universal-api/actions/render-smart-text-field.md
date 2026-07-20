# Timetonic: Render Smart Text Field

Retrieves rendered output for a smart text field from Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/render-smart-text-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/render-smart-text-field?connectionId=$CONNECTION_ID&bookOwner=mindcloud&categoryId=651496&rowId=147159065&fieldId=8729253" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookOwner": "mindcloud",
  "categoryId": "651496",
  "rowId": "147159065",
  "fieldId": "8729253"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/render-smart-text-field?${params}`, {
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
| `bookOwner` | string | yes | Book owner containing the row. Default: `mindcloud`. Example: `mindcloud`. |
| `categoryId` | string | yes | Category or table identifier. Example: `651496`. |
| `rowId` | string | yes | Row identifier containing the field value. Example: `147159065`. |
| `fieldId` | string | yes | Field identifier to render. Example: `8729253`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timetonic API returns.

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-smart-text-field.md) for the provider-specific parameters and requirements.

