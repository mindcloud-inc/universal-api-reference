# Zoho Sign: List Documents

Retrieves documents from Zoho Sign.

```
GET https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-documents?${params}`, {
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
      "code": 1,
      "message": "string",
      "pageContext": {
        "hasMoreRows": true,
        "rowCount": 1,
        "sortColumn": "string",
        "sortOrder": "string",
        "startIndex": 1,
        "totalCount": 1
      },
      "requests": [
        {
          "actions": [
            {}
          ],
          "createdTime": 1,
          "documentIds": [
            {}
          ],
          "emailReminders": true,
          "expirationDays": 1,
          "isSequential": true,
          "modifiedTime": 1,
          "ownerEmail": "ava@example.com",
          "requestId": "string",
          "requestName": "Ava Chen",
          "requestStatus": "string",
          "requestTypeId": "string",
          "requestTypeName": "Ava Chen",
          "selfSign": true,
          "signPercentage": 1
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `pageContext` | object |  |
| `pageContext.hasMoreRows` | boolean |  |
| `pageContext.rowCount` | number |  |
| `pageContext.sortColumn` | string |  |
| `pageContext.sortOrder` | string |  |
| `pageContext.startIndex` | number |  |
| `pageContext.totalCount` | number |  |
| `requests` | array<object> |  |
| `requests[].actions` | array<object> |  |
| `requests[].createdTime` | number |  |
| `requests[].documentIds` | array<object> |  |
| `requests[].emailReminders` | boolean |  |
| `requests[].expirationDays` | number |  |
| `requests[].isSequential` | boolean |  |
| `requests[].modifiedTime` | number |  |
| `requests[].ownerEmail` | string |  |
| `requests[].requestId` | string |  |
| `requests[].requestName` | string |  |
| `requests[].requestStatus` | string |  |
| `requests[].requestTypeId` | string |  |
| `requests[].requestTypeName` | string |  |
| `requests[].selfSign` | boolean |  |
| `requests[].signPercentage` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `GET /requests` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

