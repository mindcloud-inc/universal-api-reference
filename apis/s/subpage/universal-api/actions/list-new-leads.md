# Subpage: List New Leads



```
GET https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-new-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Subpage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-new-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/subpage/latest/actions/list-new-leads?${params}`, {
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
      "browser": "string",
      "city": "string",
      "country": "string",
      "countryName": "Ava Chen",
      "displayDate": "string",
      "ebook": true,
      "email": "ava@example.com",
      "id": "string",
      "os": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser` | string | Lead browser. |
| `city` | string | Lead city. |
| `country` | string | Lead country code. |
| `countryName` | string | Lead country name. |
| `displayDate` | string | Display-ready event timestamp. |
| `ebook` | boolean | Whether the lead requested an ebook. |
| `email` | string | Lead email address. |
| `id` | string | Unique Subpage lead identifier. |
| `os` | string | Lead operating system. |
| `timestamp` | number | Lead event timestamp in milliseconds. |

## Native endpoint

Through the native Subpage API, this operation is `GET /call/api/zapier/listtrigger` (base URL `https://editor.subpage.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-new-leads.md) for the provider-specific parameters and requirements.

