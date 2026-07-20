# Saleshandy: Get Prospect Minimal Sequences



```
GET https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/get-prospect-minimal-sequences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saleshandy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/get-prospect-minimal-sequences?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saleshandy/latest/actions/get-prospect-minimal-sequences?${params}`, {
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
| `contactId` | string | yes | Prospect contact ID to fetch minimal sequence histories for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "payload": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `payload` | array<object> |  |

## Native endpoint

Through the native Saleshandy API, this operation is `GET /prospects/[:contactId]/minimal/sequences` (base URL `https://open-api.saleshandy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prospect-minimal-sequences.md) for the provider-specific parameters and requirements.

