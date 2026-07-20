# turboSMTP: List Email Validation Lists

Retrieves email validation lists from turboSMTP.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-email-validation-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-email-validation-lists?connectionId=$CONNECTION_ID&from=2026-04-01&to=2026-04-02" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-01",
  "to": "2026-04-02"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-email-validation-lists?${params}`, {
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
| `from` | string | yes | Start date in YYYY-MM-DD format. Example: `2026-04-01`. |
| `to` | string | yes | End date in YYYY-MM-DD format. Example: `2026-04-02`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
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
| `count` | number | Total number of email validation lists in the selected date range. |
| `results` | array<object> | Email validation lists returned by turboSMTP. |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /emailvalidation/lists` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-validation-lists.md) for the provider-specific parameters and requirements.

