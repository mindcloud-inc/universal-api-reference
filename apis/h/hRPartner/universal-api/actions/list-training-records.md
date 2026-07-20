# HR Partner: List Training Records



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-training-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-training-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-training-records?${params}`, {
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
      "commenceDate": "2026-05-07T12:00:00.000Z",
      "comments": "string",
      "completionDate": "2026-05-07T12:00:00.000Z",
      "cost": 1,
      "courseName": "Ava Chen",
      "employee": {},
      "id": 1,
      "institution": "string",
      "reimbursement": 1,
      "trainingStatus": "string",
      "trainingType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commenceDate` | date |  |
| `comments` | string |  |
| `completionDate` | date |  |
| `cost` | number |  |
| `courseName` | string |  |
| `employee` | object |  |
| `id` | number |  |
| `institution` | string |  |
| `reimbursement` | number |  |
| `trainingStatus` | string |  |
| `trainingType` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /training` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-training-records.md) for the provider-specific parameters and requirements.

