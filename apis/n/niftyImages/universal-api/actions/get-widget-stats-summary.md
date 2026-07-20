# NiftyImages: Get Widget Stats Summary

Retrieves widget stats summary from NiftyImages.

```
GET https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-widget-stats-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-widget-stats-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/get-widget-stats-summary?${params}`, {
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
| `startDate` | string | no | Start date in ISO 8601 format. |
| `endDate` | string | no | End date in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Images": 1,
      "Impressions": 1,
      "Name": "Ava Chen",
      "Users": 1,
      "WidgetKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Images` | number |  |
| `Impressions` | number |  |
| `Name` | string |  |
| `Users` | number |  |
| `WidgetKey` | string |  |

## Native endpoint

Through the native NiftyImages API, this operation is `GET /Widgets/AllStats` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-widget-stats-summary.md) for the provider-specific parameters and requirements.

