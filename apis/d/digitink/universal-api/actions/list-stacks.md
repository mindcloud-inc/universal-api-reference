# Digit.ink: List Stacks



```
GET https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-stacks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digit.ink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-stacks?connectionId=$CONNECTION_ID&key=issued&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "issued",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitink/latest/actions/list-stacks?${params}`, {
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
| `key` | list | yes | Digit.ink stack filter key. One of: `issued`, `stackName`, `stackUuid`. |
| `value` | string | yes | Digit.ink stack filter value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchIds": [
        "string"
      ],
      "issuerUri": "string",
      "stackName": "Ava Chen",
      "stackUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchIds` | array<string> |  |
| `issuerUri` | string |  |
| `stackName` | string |  |
| `stackUuid` | string |  |

## Native endpoint

Through the native Digit.ink API, this operation is `GET /stacks` (base URL `https://app.digit.ink/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stacks.md) for the provider-specific parameters and requirements.

