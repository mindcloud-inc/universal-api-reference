# Chargback: List Alerts

Retrieves chargeback alert records from Chargback.

```
GET https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargback/latest/actions/list-alerts?${params}`, {
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
| `page` | number | no |  |
| `page_size` | number | no |  |
| `ordered_by` | string | no |  |
| `alert_status` | string | no |  |
| `alert_service` | string | no |  |
| `business_account` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
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
| `count` | number | Total number of alerts available for the current credential. |
| `next` | string | Next-page URL when more alerts are available. |
| `previous` | string | Previous-page URL when not on the first page. |
| `results` | array<object> | List of alert records returned by Chargeback. |

## Native endpoint

Through the native Chargback API, this operation is `GET /api/public/v1/alerts/` (base URL `https://api.chargeback.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alerts.md) for the provider-specific parameters and requirements.

