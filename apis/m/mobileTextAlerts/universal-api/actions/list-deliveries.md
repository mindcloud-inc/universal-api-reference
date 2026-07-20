# Mobile Text Alerts: List Deliveries

Retrieves message deliveries from Mobile Text Alerts.

```
GET https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/list-deliveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mobile Text Alerts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/list-deliveries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mobileTextAlerts/latest/actions/list-deliveries?${params}`, {
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
| `page` | number | no | Page number to retrieve. |
| `pageSize` | number | no | Number of results per page. |
| `query` | string | no | Search by subscriber name, number, or email. |
| `status` | string | no | Filter by delivery status. |
| `startDate` | string | no | Filter deliveries on or after YYYY-MM-DD. |
| `endDate` | string | no | Filter deliveries on or before YYYY-MM-DD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Delivery results page returned by Mobile Text Alerts. |
| `message` | string | Optional API response message. |

## Native endpoint

Through the native Mobile Text Alerts API, this operation is `GET /deliveries` (base URL `https://api.mobile-text-alerts.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deliveries.md) for the provider-specific parameters and requirements.

