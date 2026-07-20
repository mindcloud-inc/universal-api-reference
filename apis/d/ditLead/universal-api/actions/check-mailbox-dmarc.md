# DitLead: Check Mailbox DMARC



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-dmarc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-dmarc?connectionId=$CONNECTION_ID&domain=string&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-dmarc?${params}`, {
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
| `domain` | string | yes | Domain to verify DMARC for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "hasDmarc": true,
        "isValid": true,
        "policy": "string",
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
| `data.hasDmarc` | boolean |  |
| `data.isValid` | boolean |  |
| `data.policy` | string |  |
| `data.record` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `POST /v1/mailbox/check-dmarc` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-mailbox-dmarc.md) for the provider-specific parameters and requirements.

