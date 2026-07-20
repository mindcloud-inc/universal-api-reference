# HR Partner: List Education Records



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-education-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-education-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-education-records?${params}`, {
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
      "educationStatus": "string",
      "educationType": "string",
      "employee": {},
      "id": 1,
      "institution": "string"
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
| `educationStatus` | string |  |
| `educationType` | string |  |
| `employee` | object |  |
| `id` | number |  |
| `institution` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /education` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-education-records.md) for the provider-specific parameters and requirements.

