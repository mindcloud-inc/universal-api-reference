# Tophhie Cloud: Get Domain

Retrieves domain details from Tophhie Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-domain?connectionId=$CONNECTION_ID&domainName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/get-domain?${params}`, {
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
| `domainName` | string | yes | The domain name to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authoritativeNameServers": [
        "Ava Chen"
      ],
      "dmarcPolicy": "string",
      "isPrimaryDomain": true,
      "mxRecords": [
        "string"
      ],
      "name": "Ava Chen",
      "registeredSince": "2026-05-07T12:00:00.000Z",
      "spfRecord": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authoritativeNameServers` | array<string> | Authoritative name servers. |
| `dmarcPolicy` | string | DMARC policy. |
| `isPrimaryDomain` | boolean | Whether this is a primary domain. |
| `mxRecords` | array<string> | MX records. |
| `name` | string | Domain name. |
| `registeredSince` | date | Domain registration timestamp. |
| `spfRecord` | string | SPF record. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /domains/{domainName}` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain.md) for the provider-specific parameters and requirements.

