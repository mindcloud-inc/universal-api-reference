# Zoho ZeptoMail: Get Domain

Retrieves domain details from Zoho ZeptoMail.

```
GET https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/get-domain?connectionId=$CONNECTION_ID&domainKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/get-domain?${params}`, {
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
| `domainKey` | string | yes | Domain key from ZeptoMail. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "domain_key": "string",
        "domain_name": "Ava Chen",
        "status": "string",
        "sub_domain_prefix": "string",
        "verified": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.domain_key` | string |  |
| `data.domain_name` | string |  |
| `data.status` | string |  |
| `data.sub_domain_prefix` | string |  |
| `data.verified` | boolean |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `GET domains/:domainKey` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

