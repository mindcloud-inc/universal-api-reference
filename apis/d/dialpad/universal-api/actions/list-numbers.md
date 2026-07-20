# Dialpad: List Numbers

Retrieves company phone numbers from Dialpad.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/list-numbers?${params}`, {
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
| `status` | string | no | Filter numbers by Dialpad status. Example: `active`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor from a previous Dialpad numbers response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "areaCode": "string",
      "companyId": "string",
      "number": "string",
      "officeId": "string",
      "status": "string",
      "targetId": "string",
      "targetType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areaCode` | string |  |
| `companyId` | string |  |
| `number` | string |  |
| `officeId` | string |  |
| `status` | string |  |
| `targetId` | string |  |
| `targetType` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `GET /numbers` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-numbers.md) for the provider-specific parameters and requirements.

