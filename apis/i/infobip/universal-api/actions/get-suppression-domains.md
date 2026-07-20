# Infobip: Get Suppression Domains



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-suppression-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-suppression-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/get-suppression-domains?${params}`, {
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
        "createBounces": true,
        "createComplaints": true,
        "dataAccess": "string",
        "deleteBounces": true,
        "deleteComplaints": true,
        "deleteOverquotas": true,
        "domainName": "Ava Chen",
        "readBounces": true,
        "readComplaints": true,
        "readOverquotas": true
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
| `results.createBounces` | boolean |  |
| `results.createComplaints` | boolean |  |
| `results.dataAccess` | string |  |
| `results.deleteBounces` | boolean |  |
| `results.deleteComplaints` | boolean |  |
| `results.deleteOverquotas` | boolean |  |
| `results.domainName` | string |  |
| `results.readBounces` | boolean |  |
| `results.readComplaints` | boolean |  |
| `results.readOverquotas` | boolean |  |

## Native endpoint

Through the native Infobip API, this operation is `GET /email/1/suppressions/domains` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-suppression-domains.md) for the provider-specific parameters and requirements.

