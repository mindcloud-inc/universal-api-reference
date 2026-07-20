# Vtiger CRM: List Quotes

Finds quotes in Vtiger CRM by query.

```
GET https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/list-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vtiger CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/list-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/list-quotes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Vtiger Quote id. |
| `subject` | string | Quote subject. |

## Native endpoint

Through the native Vtiger CRM API, this operation is `GET /query?query=select+id%2C+subject+from+Quotes+limit+0%2C+25%3B` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quotes.md) for the provider-specific parameters and requirements.

