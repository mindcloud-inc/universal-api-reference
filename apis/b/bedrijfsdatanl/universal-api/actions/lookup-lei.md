# Bedrijfsdata.nl: Lookup LEI



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-lei
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-lei?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-lei?${params}`, {
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
| `name` | string | no | Organization name to search for an LEI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "lei": {
        "address": "string",
        "city": "string",
        "countryCode": "string",
        "lei": "string",
        "leiRecordUrl": "https://example.com",
        "name": "Ava Chen",
        "renewalDate": "2026-05-07T12:00:00.000Z",
        "status": "string",
        "success": 1
      },
      "monthlyCredits": 1,
      "product": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `lei.address` | string |  |
| `lei.city` | string |  |
| `lei.countryCode` | string |  |
| `lei.lei` | string |  |
| `lei.leiRecordUrl` | string |  |
| `lei.name` | string |  |
| `lei.renewalDate` | date |  |
| `lei.status` | string |  |
| `lei.success` | number |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /lei` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-lei.md) for the provider-specific parameters and requirements.

