# KickFire: Get Company by Website

Retrieves company firmographic data from KickFire by website.

```
GET https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-company-by-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KickFire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-company-by-website?connectionId=$CONNECTION_ID&website=example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "website": "example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-company-by-website?${params}`, {
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
| `website` | string | yes | Website or domain to enrich, without protocol or path. Example: `example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
      "results": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].companyName` | string |  |
| `data[].dstOffset` | number |  |
| `data[].isISP` | number |  |
| `data[].isMobile` | number |  |
| `data[].isWifi` | number |  |
| `data[].timeZoneId` | string |  |
| `data[].timeZoneName` | string |  |
| `data[].tradeName` | string |  |
| `data[].utcOffset` | string |  |
| `data[].website` | string |  |
| `results` | number |  |
| `status` | string |  |

## Native endpoint

Through the native KickFire API, this operation is `GET /v3/company` (base URL `https://api.kickfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-by-website.md) for the provider-specific parameters and requirements.

