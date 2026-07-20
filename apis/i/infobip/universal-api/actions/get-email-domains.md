# Infobip: Get Email Domains



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-domains?${params}`, {
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
| `size` | number | no | Maximum number of domains to be viewed per page. Default value is 10 with a maximum of 20 records per page. |
| `page` | number | no | Page number you want to see. Default is 0. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {
        "page": 1,
        "size": 1,
        "totalPages": 1,
        "totalResults": 1
      },
      "results": {
        "active": true,
        "blocked": true,
        "blocklistConfigurationLevel": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "dnsRecords": [
          {}
        ],
        "domainId": 1,
        "domainName": "Ava Chen",
        "tracking": {
          "clicks": true,
          "opens": true,
          "unsubscribe": true
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paging` | object |  |
| `paging.page` | number |  |
| `paging.size` | number |  |
| `paging.totalPages` | number |  |
| `paging.totalResults` | number |  |
| `results` | array<object> |  |
| `results.active` | boolean |  |
| `results.blocked` | boolean |  |
| `results.blocklistConfigurationLevel` | string |  |
| `results.createdAt` | date |  |
| `results.dnsRecords` | array<object> |  |
| `results.domainId` | number |  |
| `results.domainName` | string |  |
| `results.tracking` | object |  |
| `results.tracking.clicks` | boolean |  |
| `results.tracking.opens` | boolean |  |
| `results.tracking.unsubscribe` | boolean |  |

## Native endpoint

Through the native Infobip API, this operation is `GET /email/1/domains` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-domains.md) for the provider-specific parameters and requirements.

