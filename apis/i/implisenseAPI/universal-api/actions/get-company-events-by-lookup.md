# Implisense: Get Company Events By Lookup

Finds company events in Implisense API by lookup.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-events-by-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-events-by-lookup?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-events-by-lookup?${params}`, {
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
| `query` | string | yes | Known company text, for example a company name and city. |
| `name` | string | no | Official company name. |
| `city` | string | no | City of the company headquarters. |
| `active` | boolean | no | Return only companies that are still active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {},
      "publisher": "string",
      "source": "string",
      "text": "string",
      "timestamp": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | object |  |
| `publisher` | string |  |
| `source` | string |  |
| `text` | string |  |
| `timestamp` | number |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Implisense API, this operation is `POST /companies/events` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-events-by-lookup.md) for the provider-specific parameters and requirements.

