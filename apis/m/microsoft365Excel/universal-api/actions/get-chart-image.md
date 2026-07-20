# Microsoft 365 Excel: Get Chart Image

Retrieves a chart image from Microsoft 365 Excel.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/get-chart-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/get-chart-image?connectionId=$CONNECTION_ID&driveItemId=string&worksheetName=RuntimeVerify&chartName=Chart%201&width=640&height=480&fittingMode=Fit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveItemId": "string",
  "worksheetName": "RuntimeVerify",
  "chartName": "Chart 1",
  "width": "640",
  "height": "480",
  "fittingMode": "Fit"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/get-chart-image?${params}`, {
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
| `driveItemId` | string | yes |  |
| `worksheetName` | string | yes | Example: `RuntimeVerify`. |
| `chartName` | string | yes | Example: `Chart 1`. |
| `width` | number | yes | Default: `640`. |
| `height` | number | yes | Default: `480`. |
| `fittingMode` | string | yes | Default: `Fit`. Example: `Fit`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Base64-encoded chart image string. |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts('{{chartName}}')/image(width={{width}},height={{height}},fittingMode='{{fittingMode}}')` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chart-image.md) for the provider-specific parameters and requirements.

