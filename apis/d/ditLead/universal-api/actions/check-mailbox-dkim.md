# DitLead: Check Mailbox DKIM



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-dkim
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-dkim?connectionId=$CONNECTION_ID&domain=string&domain=string&selector=string&selector=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "domain": "string",
  "selector": "string",
  "selector": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-dkim?${params}`, {
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
| `domain` | string | yes |  |
| `domain` | string | yes | Domain to verify DKIM for. |
| `selector` | string | yes |  |
| `selector` | string | yes | DKIM selector to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "hasDkim": true,
        "isValid": true,
        "record": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.hasDkim` | boolean |  |
| `data.isValid` | boolean |  |
| `data.record` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `POST /v1/mailbox/check-dkim` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-mailbox-dkim.md) for the provider-specific parameters and requirements.

