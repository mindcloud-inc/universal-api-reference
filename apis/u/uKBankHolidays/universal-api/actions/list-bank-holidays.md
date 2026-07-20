# UK Bank Holidays: List Bank Holidays

Retrieves UK bank holiday dates from UK Bank Holidays.

```
GET https://connect.mindcloud.co/v1/universal/uKBankHolidays/latest/actions/list-bank-holidays
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UK Bank Holidays `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKBankHolidays/latest/actions/list-bank-holidays?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKBankHolidays/latest/actions/list-bank-holidays?${params}`, {
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
      "bunting": true,
      "date": "string",
      "division": "string",
      "notes": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bunting` | boolean |  |
| `date` | string |  |
| `division` | string |  |
| `notes` | string |  |
| `title` | string |  |

## Native endpoint

Through the native UK Bank Holidays API, this operation is `GET /bank-holidays.json` (base URL `https://www.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bank-holidays.md) for the provider-specific parameters and requirements.

