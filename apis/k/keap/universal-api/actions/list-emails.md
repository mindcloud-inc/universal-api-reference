# Keap: List Emails



```
GET https://connect.mindcloud.co/v1/universal/keap/latest/actions/list-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/list-emails?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keap/latest/actions/list-emails?${params}`, {
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
      "contactId": "string",
      "id": "string",
      "originalProvider": "string",
      "sentDate": "2026-05-07T12:00:00.000Z",
      "sentFromAddress": "string",
      "sentTime": "2026-05-07T12:00:00.000Z",
      "sentToAddress": "string",
      "sentToBccAddresses": "string",
      "sentToCcAddresses": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | string |  |
| `id` | string |  |
| `originalProvider` | string |  |
| `sentDate` | date |  |
| `sentFromAddress` | string |  |
| `sentTime` | date |  |
| `sentToAddress` | string |  |
| `sentToBccAddresses` | string |  |
| `sentToCcAddresses` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native Keap API, this operation is `GET /emails` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-emails.md) for the provider-specific parameters and requirements.

