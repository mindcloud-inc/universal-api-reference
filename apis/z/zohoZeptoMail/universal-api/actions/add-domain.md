# Zoho ZeptoMail: Add Domain

Adds a new domain in Zoho ZeptoMail.

```
POST https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainName": "Ava Chen",
  "subDomainPrefix": "string",
  "mailagent_keys[0]": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/add-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainName": "Ava Chen",
    "subDomainPrefix": "string",
    "mailagent_keys[0]": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainName` | string | yes | Domain to add to ZeptoMail. |
| `subDomainPrefix` | string | yes | Subdomain prefix used for bounce tracking. |
| `mailagent_keys[0]` | string | yes | Agent alias to associate with the domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "domain_key": "string",
        "domain_name": "Ava Chen",
        "mailagent_keys": [
          "string"
        ],
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
| `data.mailagent_keys[]` | string |  |
| `data.status` | string |  |
| `data.sub_domain_prefix` | string |  |
| `data.verified` | boolean |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `POST domains` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-domain.md) for the provider-specific parameters and requirements.

