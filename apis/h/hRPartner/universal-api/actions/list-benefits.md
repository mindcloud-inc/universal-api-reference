# HR Partner: List Benefits



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-benefits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-benefits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-benefits?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "benefitProvider": "string",
      "benefitStatus": "string",
      "benefitType": "string",
      "benefitValue": 1,
      "benefitValuePeriod": "string",
      "description": "string",
      "employee": {},
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `benefitProvider` | string |  |
| `benefitStatus` | string |  |
| `benefitType` | string |  |
| `benefitValue` | number |  |
| `benefitValuePeriod` | string |  |
| `description` | string |  |
| `employee` | object |  |
| `endDate` | date |  |
| `id` | number |  |
| `startDate` | date |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /benefits` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-benefits.md) for the provider-specific parameters and requirements.

