# Zoho ZeptoMail: Update Domain

Updates an existing domain in Zoho ZeptoMail.

```
PUT https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/update-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/update-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/update-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainKey` | string | yes | Domain key from ZeptoMail. |
| `newDomain` | string | no | Replacement domain name. |
| `newSubDomainPrefix` | string | no | Replacement bounce subdomain prefix. |
| `associate_mailagents[0]` | string | no | Agent alias to associate with the domain. |
| `unassociate_mailagents[0]` | string | no | Agent alias to disassociate from the domain. |

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

Through the native Zoho ZeptoMail API, this operation is `PUT domains/:domainKey` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain.md) for the provider-specific parameters and requirements.

