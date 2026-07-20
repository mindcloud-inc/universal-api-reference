# MailerSend: Get Analytics By Country



```
GET https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-analytics-by-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-analytics-by-country?connectionId=$CONNECTION_ID&dateFrom=string&dateTo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "string",
  "dateTo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/get-analytics-by-country?${params}`, {
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
| `dateFrom` | string | yes | Start datetime for analytics results in YYYY-MM-DD HH:mm:ss format. |
| `dateTo` | string | yes | End datetime for analytics results in YYYY-MM-DD HH:mm:ss format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateFrom": 1,
      "dateTo": 1,
      "stats": [
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
| `dateFrom` | number |  |
| `dateTo` | number |  |
| `stats` | array<object> |  |

## Native endpoint

Through the native MailerSend API, this operation is `GET /analytics/country` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics-by-country.md) for the provider-specific parameters and requirements.

