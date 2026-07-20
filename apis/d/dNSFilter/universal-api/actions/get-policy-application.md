# DNSFilter: Get Policy Application



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-policy-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-policy-application?connectionId=$CONNECTION_ID&applicationId=1&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationId": "1",
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-policy-application?${params}`, {
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
| `applicationId` | number | yes | Application ID |
| `organizationId` | number | yes | Organization ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_policies": [
        {}
      ],
      "application": {},
      "block_policies": [
        {}
      ],
      "organization": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allow_policies` | array<object> |  |
| `application` | object |  |
| `block_policies` | array<object> |  |
| `organization` | object |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/policies/application` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-policy-application.md) for the provider-specific parameters and requirements.

