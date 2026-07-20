# GMass: List Google Sheets

Retrieves Google Sheets connected to GMass.

```
GET https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-google-sheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GMass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-google-sheets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-google-sheets?${params}`, {
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
      "spreadsheetId": "string",
      "spreadsheetName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `spreadsheetId` | string | Google Sheet ID. |
| `spreadsheetName` | string | Google Sheet name. |

## Native endpoint

Through the native GMass API, this operation is `GET /sheets` (base URL `https://api.gmass.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-sheets.md) for the provider-specific parameters and requirements.

