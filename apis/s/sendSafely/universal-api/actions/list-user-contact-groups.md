# SendSafely: List User Contact Groups



```
GET https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/list-user-contact-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/list-user-contact-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/list-user-contact-groups?${params}`, {
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
      "contactGroups": [
        {}
      ],
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactGroups` | array<object> |  |
| `response` | string |  |

## Native endpoint

Through the native SendSafely API, this operation is `GET /user/groups/` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-contact-groups.md) for the provider-specific parameters and requirements.

