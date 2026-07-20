# Implisense: Get Company Events

Retrieves company events from Implisense API.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-events?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-events?${params}`, {
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
| `id` | string | yes | Implisense company identifier, for example DEVFCLQFW054. |
| `type` | string | no | Optional event type, such as BLOG or NEWS. |
| `category` | string | no | Optional event category code, such as MANAGEMENT_AND_TEAM. |
| `since` | string | no | Optional lower timestamp boundary for returned events. |
| `size` | number | no | Maximum number of events to return. Default: `10`. |

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

Through the native Implisense API, this operation is `GET /companies/:id/events` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-events.md) for the provider-specific parameters and requirements.

