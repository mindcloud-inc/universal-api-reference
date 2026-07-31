# Numbers API: Get Year Fact



```
GET https://connect.mindcloud.co/v1/universal/numbersAPI/latest/actions/get-year-fact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Numbers API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/numbersAPI/latest/actions/get-year-fact?connectionId=$CONNECTION_ID&year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/numbersAPI/latest/actions/get-year-fact?${params}`, {
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
| `year` | number | yes |  |
| `fragment` | boolean | no |  |
| `notfound` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "found": true,
      "number": 1,
      "text": "string",
      "type": "string",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `found` | boolean |  |
| `number` | number |  |
| `text` | string |  |
| `type` | string |  |
| `year` | number |  |

## Native endpoint

Through the native Numbers API API, this operation is `GET /:year/year` (base URL `http://numbersapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-year-fact.md) for the provider-specific parameters and requirements.

