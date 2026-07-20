# PayTabs: Search Invoices



```
GET https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/search-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/search-invoices?connectionId=$CONNECTION_ID&created_date_from=string&created_date_to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "created_date_from": "string",
  "created_date_to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/search-invoices?${params}`, {
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
| `created_date_from` | string | yes | Lower bound creation date in the PayTabs search format. |
| `created_date_to` | string | yes | Upper bound creation date in the PayTabs search format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "invoices": [
        {}
      ],
      "message": "string",
      "trace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `invoices` | array<object> |  |
| `message` | string |  |
| `trace` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/invoice/search` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-invoices.md) for the provider-specific parameters and requirements.

