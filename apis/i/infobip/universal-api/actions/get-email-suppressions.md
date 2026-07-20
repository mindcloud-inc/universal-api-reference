# Infobip: Get Email Suppressions



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-suppressions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-suppressions?connectionId=$CONNECTION_ID&domainName=Ava%20Chen&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domainName": "Ava Chen",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-email-suppressions?${params}`, {
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
| `domainName` | string | yes | Name of the requested domain. |
| `type` | string | yes | Type of suppression. |
| `emailAddress` | string | no | Email address that is suppressed. |
| `recipientDomain` | string | no | Recipient domain that is suppressed. |
| `createdDateFrom` | date | no | Start date for searching suppressions. |
| `createdDateTo` | date | no | End date for searching suppressions. |
| `page` | number | no | Requested page number. |
| `size` | number | no | Requested page size. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {
        "page": 1,
        "size": 1
      },
      "results": {
        "createdDate": "2026-05-07T12:00:00.000Z",
        "domainName": "Ava Chen",
        "emailAddress": "ava@example.com",
        "reason": "string",
        "type": "string"
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
| `results` | array<object> |  |
| `results.createdDate` | date |  |
| `results.domainName` | string |  |
| `results.emailAddress` | string |  |
| `results.reason` | string |  |
| `results.type` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `GET /email/1/suppressions` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-suppressions.md) for the provider-specific parameters and requirements.

