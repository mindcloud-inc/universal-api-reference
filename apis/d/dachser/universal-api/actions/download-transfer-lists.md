# Dachser: Download Transfer Lists

Downloads transfer lists for a specific date from Dachser.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/download-transfer-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/download-transfer-lists?connectionId=$CONNECTION_ID&orderdate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderdate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/download-transfer-lists?${params}`, {
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
| `orderdate` | date | yes | Transfer list order date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `acceptLanguage` | string | no | Optional language sent as the Accept-Language header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consolidator": "string",
      "transferList": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `consolidator` | string |  |
| `transferList` | string |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/transferlists/{orderdate}` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-transfer-lists.md) for the provider-specific parameters and requirements.

