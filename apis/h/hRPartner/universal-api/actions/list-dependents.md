# HR Partner: List Dependents



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-dependents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-dependents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-dependents?${params}`, {
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
      "comments": "string",
      "contactDetails": "string",
      "dateOfBirth": "2026-05-07T12:00:00.000Z",
      "dependentType": "string",
      "employee": {},
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `comments` | string |  |
| `contactDetails` | string |  |
| `dateOfBirth` | date |  |
| `dependentType` | string |  |
| `employee` | object |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /dependents` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dependents.md) for the provider-specific parameters and requirements.

