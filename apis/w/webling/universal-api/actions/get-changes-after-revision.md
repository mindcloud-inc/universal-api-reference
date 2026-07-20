# Webling: Get Changes After Revision



```
GET https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-changes-after-revision
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-changes-after-revision?connectionId=$CONNECTION_ID&id=1530" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1530"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webling/latest/actions/get-changes-after-revision?${params}`, {
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
| `id` | number | yes | Example: `1530`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": [
        {}
      ],
      "definitions": [
        {}
      ],
      "deleted": [
        1
      ],
      "objects": [
        {}
      ],
      "quota": true,
      "revision": 1,
      "settings": true,
      "subscription": true,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | array<object> |  |
| `definitions` | array<object> |  |
| `deleted` | array<number> |  |
| `objects` | array<object> |  |
| `quota` | boolean |  |
| `revision` | number |  |
| `settings` | boolean |  |
| `subscription` | boolean |  |
| `version` | number |  |

## Native endpoint

Through the native Webling API, this operation is `GET /replicate/:id` (base URL `https://{{credentials.instanceDomain}}/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-changes-after-revision.md) for the provider-specific parameters and requirements.

