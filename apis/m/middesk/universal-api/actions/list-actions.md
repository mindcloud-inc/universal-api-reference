# Middesk: List actions for an object

Retrieves actions for an object from Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-actions?connectionId=$CONNECTION_ID&objectId=string&objectType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectId": "string",
  "objectType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-actions?${params}`, {
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
| `objectId` | string | yes | ID of the object whose actions you want to list. |
| `objectType` | string | yes | Type of object whose actions you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `object` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /actions` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-actions.md) for the provider-specific parameters and requirements.

