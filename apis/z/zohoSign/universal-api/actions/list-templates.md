# Zoho Sign: List Templates

Retrieves templates from Zoho Sign.

```
GET https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/list-templates?${params}`, {
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
      "status": "string",
      "templates": [
        {
          "actions": [
            {}
          ],
          "createdTime": 1,
          "description": "string",
          "documentIds": [
            {}
          ],
          "emailReminders": true,
          "expirationDays": 1,
          "isSequential": true,
          "modifiedTime": 1,
          "notes": "string",
          "ownerEmail": "ava@example.com",
          "requestTypeId": "string",
          "requestTypeName": "Ava Chen",
          "templateId": "string",
          "templateName": "Ava Chen"
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
| `code` | number |  |
| `message` | string |  |
| `pageContext` | object |  |
| `pageContext.hasMoreRows` | boolean |  |
| `pageContext.rowCount` | number |  |
| `pageContext.sortColumn` | string |  |
| `pageContext.sortOrder` | string |  |
| `pageContext.startIndex` | number |  |
| `pageContext.totalCount` | number |  |
| `status` | string |  |
| `templates` | array<object> |  |
| `templates[].actions` | array<object> |  |
| `templates[].createdTime` | number |  |
| `templates[].description` | string |  |
| `templates[].documentIds` | array<object> |  |
| `templates[].emailReminders` | boolean |  |
| `templates[].expirationDays` | number |  |
| `templates[].isSequential` | boolean |  |
| `templates[].modifiedTime` | number |  |
| `templates[].notes` | string |  |
| `templates[].ownerEmail` | string |  |
| `templates[].requestTypeId` | string |  |
| `templates[].requestTypeName` | string |  |
| `templates[].templateId` | string |  |
| `templates[].templateName` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `GET /templates` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

