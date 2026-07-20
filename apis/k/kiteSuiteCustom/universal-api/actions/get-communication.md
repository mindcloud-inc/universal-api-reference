# Kite Suite: Get communication



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-communication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-communication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-communication?${params}`, {
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
      "bcc": [
        "string"
      ],
      "body": "string",
      "cc": [
        "string"
      ],
      "lastUpdated": "string",
      "recievers": [
        "string"
      ],
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcc` | array<string> |  |
| `body` | string |  |
| `cc` | array<string> |  |
| `lastUpdated` | string |  |
| `recievers` | array<string> |  |
| `subject` | string |  |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/communication` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-communication.md) for the provider-specific parameters and requirements.

