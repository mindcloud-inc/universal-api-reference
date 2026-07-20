# Bedrijfsdata.nl: Find Company People



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/find-company-people?${params}`, {
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
| `name` | string | no | Company name used to find people records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "emailformat": "ava@example.com",
      "employees": {},
      "found": 1,
      "monthlyCredits": 1,
      "namecounts": {
        "changedDate": "2026-05-07T12:00:00.000Z",
        "cocCount": {},
        "name": "Ava Chen",
        "nameids": {},
        "nameMain": "Ava Chen",
        "names": "Ava Chen",
        "text": "Ava Chen"
      },
      "product": "string",
      "status": "string",
      "total": 1
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
| `emailformat` | string |  |
| `employees` | object |  |
| `found` | number |  |
| `monthlyCredits` | number |  |
| `namecounts.changedDate` | date |  |
| `namecounts.cocCount` | object |  |
| `namecounts.name` | string |  |
| `namecounts.nameids` | object |  |
| `namecounts.nameMain` | string |  |
| `namecounts.names` | string |  |
| `namecounts.text` | string |  |
| `product` | string |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /people` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-company-people.md) for the provider-specific parameters and requirements.

