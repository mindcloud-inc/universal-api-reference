# Metance: Get Current Company

Retrieves the current company from Metance.

```
GET https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metance `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-current-company?${params}`, {
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
      "countryCode": "string",
      "id": 1,
      "logoPath": "string",
      "membersCount": 1,
      "name": "Ava Chen",
      "status": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryCode` | string | Country code |
| `id` | number | Company ID |
| `logoPath` | string | Company logo path |
| `membersCount` | number | Member count |
| `name` | string | Company name |
| `status` | number | Company status |
| `title` | string | Company title |

## Native endpoint

Through the native Metance API, this operation is `GET /master/currentcompany` (base URL `https://api.metance.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-company.md) for the provider-specific parameters and requirements.

