# Yousign: Get Label

Retrieves a label from Yousign.

```
GET https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yousign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-label?connectionId=$CONNECTION_ID&labelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "labelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yousign/latest/actions/get-label?${params}`, {
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
| `labelId` | string | yes | The Yousign label ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Label creation timestamp. |
| `id` | string | Label ID. |
| `name` | string | Label name. |

## Native endpoint

Through the native Yousign API, this operation is `GET /labels/:labelId` (base URL `https://api-sandbox.yousign.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-label.md) for the provider-specific parameters and requirements.

