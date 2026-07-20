# Postmark: Get Bounce

Retrieves a bounce from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-bounce
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-bounce?connectionId=$CONNECTION_ID&bounceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bounceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-bounce?${params}`, {
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
| `bounceId` | string | yes | The Postmark bounce ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BouncedAt": "2026-05-07T12:00:00.000Z",
      "CanActivate": true,
      "Description": "string",
      "Email": "ava@example.com",
      "ID": "string",
      "Inactive": true,
      "MessageID": "string",
      "Subject": "string",
      "Type": "string",
      "TypeCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BouncedAt` | date |  |
| `CanActivate` | boolean |  |
| `Description` | string |  |
| `Email` | string |  |
| `ID` | string |  |
| `Inactive` | boolean |  |
| `MessageID` | string |  |
| `Subject` | string |  |
| `Type` | string |  |
| `TypeCode` | number |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /bounces/:bounceId` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bounce.md) for the provider-specific parameters and requirements.

