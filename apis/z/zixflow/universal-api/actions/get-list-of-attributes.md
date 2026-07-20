# Zixflow: Get List of Attributes

Retrieves attributes from Zixflow.

```
GET https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-attributes?connectionId=$CONNECTION_ID&target=string&targetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "targetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-of-attributes?${params}`, {
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
| `target` | string | yes | Target resource type for attributes. |
| `targetId` | string | yes | Target resource identifier for attributes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array | Attribute rows returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the attributes request succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `GET /attributes/:target/:targetId` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-of-attributes.md) for the provider-specific parameters and requirements.

