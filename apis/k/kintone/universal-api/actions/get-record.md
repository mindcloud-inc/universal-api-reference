# Kintone: Get Record

Retrieves a record from Kintone.

```
GET https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-record?connectionId=$CONNECTION_ID&appId=1&recordId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1",
  "recordId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-record?${params}`, {
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
| `appId` | number | yes | The Kintone app ID. |
| `recordId` | number | yes | The Kintone record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "record": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `record` | object | The matching Kintone record object. |

## Native endpoint

Through the native Kintone API, this operation is `GET /record.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

