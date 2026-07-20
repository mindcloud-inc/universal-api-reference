# DitLead: Check Mailbox SPF



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-spf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-spf?connectionId=$CONNECTION_ID&domain=string&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/check-mailbox-spf?${params}`, {
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
| `domain` | string | yes | Domain to verify SPF for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "hasSpf": true,
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
| `data.hasSpf` | boolean |  |
| `data.isValid` | boolean |  |
| `data.record` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `POST /v1/mailbox/check-spf` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-mailbox-spf.md) for the provider-specific parameters and requirements.

