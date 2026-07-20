# Hyperstack Certificates: View Credential Group



```
GET https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/view-credential-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperstack Certificates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/view-credential-group?connectionId=$CONNECTION_ID&group_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/view-credential-group?${params}`, {
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
| `group_key` | string | yes | The unique key of the credential group to view. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "doesExpire": true,
      "groupCode": "string",
      "success": true,
      "tags": "string",
      "title": "string",
      "url": "https://example.com",
      "validity": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Credential group description HTML. |
| `doesExpire` | boolean | Whether issued credentials in the group expire. |
| `groupCode` | string | Credential group code. |
| `success` | boolean | Whether the credential group was loaded successfully. |
| `tags` | string | Comma-separated credential group tags. |
| `title` | string | Credential group title. |
| `url` | string | Credential group website URL. |
| `validity` | number | Group validity duration according to Hyperstack settings. |

## Native endpoint

Through the native Hyperstack Certificates API, this operation is `GET /group/view/:group_key` (base URL `https://api.thehyperstack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-credential-group.md) for the provider-specific parameters and requirements.

