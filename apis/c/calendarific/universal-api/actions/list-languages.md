# Calendarific: List Languages

Retrieves supported languages from Calendarific.

```
GET https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendarific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendarific/latest/actions/list-languages?${params}`, {
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
      "code": "string",
      "name": "Ava Chen",
      "nativeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Language code. |
| `name` | string | Language name. |
| `nativeName` | string | Language native name. |

## Native endpoint

Through the native Calendarific API, this operation is `GET /languages` (base URL `https://calendarific.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-languages.md) for the provider-specific parameters and requirements.

