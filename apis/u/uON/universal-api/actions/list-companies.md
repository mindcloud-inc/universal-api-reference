# U-ON: List Companies

Retrieves company records stored in U-ON.

```
GET https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a U-ON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-companies?${params}`, {
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
      "address_p": "string",
      "address_u": "string",
      "city": "string",
      "fullname": "Ava Chen",
      "id": 1,
      "inn": "string",
      "kpp": "string",
      "name": "Ava Chen",
      "name_rus": "Ava Chen",
      "phones": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_p` | string | Фактический адрес / Build address |
| `address_u` | string | Юридический адрес / Company address |
| `city` | string | Город / City |
| `fullname` | string | Название полное / Full name |
| `id` | number | ID / ID |
| `inn` | string | ИНН / INN |
| `kpp` | string | КПП / Bank KPP |
| `name` | string | Название / Name |
| `name_rus` | string | Название (ru) / Name (ru) |
| `phones` | string | Телефоны / Phones |

## Native endpoint

Through the native U-ON API, this operation is `GET /company.json` (base URL `https://api.u-on.ru/{key}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

