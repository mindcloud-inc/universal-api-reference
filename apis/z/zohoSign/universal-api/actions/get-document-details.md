# Zoho Sign: Get Document Details

Retrieves document details from Zoho Sign.

```
GET https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/get-document-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/get-document-details?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/get-document-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Zoho Sign request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "requests": {
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
        "signPercentage": 1,
        "zsDocumentId": "string"
      },
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
| `requests` | object |  |
| `requests.actions` | array<object> |  |
| `requests.createdTime` | number |  |
| `requests.documentIds` | array<object> |  |
| `requests.emailReminders` | boolean |  |
| `requests.expirationDays` | number |  |
| `requests.isSequential` | boolean |  |
| `requests.modifiedTime` | number |  |
| `requests.ownerEmail` | string |  |
| `requests.requestId` | string |  |
| `requests.requestName` | string |  |
| `requests.requestStatus` | string |  |
| `requests.requestTypeId` | string |  |
| `requests.requestTypeName` | string |  |
| `requests.selfSign` | boolean |  |
| `requests.signPercentage` | number |  |
| `requests.zsDocumentId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `GET /requests/:requestId` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-details.md) for the provider-specific parameters and requirements.

