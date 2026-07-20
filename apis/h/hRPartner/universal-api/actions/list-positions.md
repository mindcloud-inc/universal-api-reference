# HR Partner: List Positions



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-positions?${params}`, {
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
      "commenceDate": "2026-05-07T12:00:00.000Z",
      "comments": "string",
      "completionDate": "2026-05-07T12:00:00.000Z",
      "employee": {},
      "id": 1,
      "payLevel": "string",
      "position": "string",
      "remuneration": 1,
      "remunerationPeriod": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `commenceDate` | date |  |
| `comments` | string |  |
| `completionDate` | date |  |
| `employee` | object |  |
| `id` | number |  |
| `payLevel` | string |  |
| `position` | string |  |
| `remuneration` | number |  |
| `remunerationPeriod` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /positions` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-positions.md) for the provider-specific parameters and requirements.

