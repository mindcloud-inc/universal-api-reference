# Kite Suite: Get communications of a specific thread.



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-communications-of-a-specific-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-communications-of-a-specific-thread?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-communications-of-a-specific-thread?${params}`, {
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
| `id` | string | yes | thread ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "accountID": {},
      "communicationID": {},
      "createdBy": "string",
      "itemID": {},
      "sentAt": "string",
      "status": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `accountID` | object |  |
| `communicationID` | object |  |
| `createdBy` | string |  |
| `itemID` | object |  |
| `sentAt` | string |  |
| `status` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/communication/email/thread/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-communications-of-a-specific-thread.md) for the provider-specific parameters and requirements.

