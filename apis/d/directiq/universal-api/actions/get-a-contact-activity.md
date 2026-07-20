# DirectIQ: Get a contact activity

Retrieves a contact activity from DirectIQ by ID.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-contact-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-contact-activity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-a-contact-activity?${params}`, {
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
      "action": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "masterDataContent": "string",
      "masterDataId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `createdDate` | date |  |
| `masterDataContent` | string |  |
| `masterDataId` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /contacts/contactactivity/get/{id}` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-contact-activity.md) for the provider-specific parameters and requirements.

