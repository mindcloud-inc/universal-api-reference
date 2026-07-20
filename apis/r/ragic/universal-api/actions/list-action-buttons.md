# Ragic: List Action Buttons

Retrieves action buttons from Ragic.

```
GET https://connect.mindcloud.co/v1/universal/ragic/latest/actions/list-action-buttons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/list-action-buttons?connectionId=$CONNECTION_ID&tabFolderPath=ragic-setup&sheetIndex=8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ragic/latest/actions/list-action-buttons?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | no | The action-button category. Ragic documents `massOperation` for this listing endpoint. Default: `massOperation`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionButtons": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionButtons` | array<object> | The action buttons available for the requested sheet and category. |

## Native endpoint

Through the native Ragic API, this operation is `GET /:tabFolderPath/:sheetIndex/metadata/actionButton` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-action-buttons.md) for the provider-specific parameters and requirements.

