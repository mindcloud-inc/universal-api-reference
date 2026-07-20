# UpGuard: Retrieve IP Details

Retrieves details for an IP address in UpGuard.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-ip-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-ip-details?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/retrieve-ip-details?${params}`, {
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
| `ip` | string | yes | The IP address to get details for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": 1,
      "asName": "Ava Chen",
      "country": "string",
      "domains": [
        {
          "automatedScore": 1,
          "hostname": "Ava Chen"
        }
      ],
      "ip": "string",
      "owner": "string",
      "services": [
        "string"
      ],
      "sources": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | number |  |
| `asName` | string |  |
| `country` | string |  |
| `domains[].automatedScore` | number |  |
| `domains[].hostname` | string |  |
| `ip` | string |  |
| `owner` | string |  |
| `services[]` | string |  |
| `sources[]` | string |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /ip` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-ip-details.md) for the provider-specific parameters and requirements.

