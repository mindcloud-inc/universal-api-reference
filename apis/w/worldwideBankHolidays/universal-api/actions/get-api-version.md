# Worldwide Bank Holidays: Get API Version



```
GET https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/get-api-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worldwide Bank Holidays `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/get-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldwideBankHolidays/latest/actions/get-api-version?${params}`, {
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
      "name": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Library or service name. |
| `version` | string | Current version string. |

## Native endpoint

Through the native Worldwide Bank Holidays API, this operation is `GET /api/v3/Version` (base URL `https://date.nager.at`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-version.md) for the provider-specific parameters and requirements.

