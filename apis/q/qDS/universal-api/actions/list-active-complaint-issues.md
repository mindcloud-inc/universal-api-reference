# QDS: List Active Complaint Issues



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-active-complaint-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-active-complaint-issues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-active-complaint-issues?${params}`, {
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
      "complaintissues": [
        {
          "default": 1,
          "id": 1,
          "name": "Ava Chen",
          "polarity": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `complaintissues[].default` | number |  |
| `complaintissues[].id` | number |  |
| `complaintissues[].name` | string |  |
| `complaintissues[].polarity` | string |  |

## Native endpoint

Through the native QDS API, this operation is `GET /complaintissues/active` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-complaint-issues.md) for the provider-specific parameters and requirements.

