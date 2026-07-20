# DMSales: Get Contact Involvement

Retrieves contact involvement details from DMSales.

```
GET https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-contact-involvement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMSales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-contact-involvement?connectionId=$CONNECTION_ID&baseKey=string&dateFrom=2026-05-07T12%3A00%3A00.000Z&dateTo=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseKey": "string",
  "dateFrom": "2026-05-07T12:00:00.000Z",
  "dateTo": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dMSales/latest/actions/get-contact-involvement?${params}`, {
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
| `dateFrom` | date | yes | Start date (YYYY-MM-DD). |
| `dateTo` | date | yes | End date (YYYY-MM-DD). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "involvement": [
        {}
      ],
      "last_contact": "2026-05-07T12:00:00.000Z",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `involvement` | array<object> |  |
| `last_contact` | date |  |
| `total` | number |  |

## Native endpoint

Through the native DMSales API, this operation is `GET /api/contact-card/involvement` (base URL `https://app.dmsales.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-involvement.md) for the provider-specific parameters and requirements.

