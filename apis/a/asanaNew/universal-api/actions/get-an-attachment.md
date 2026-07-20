# Asana: Get an attachment

Retrieves an attachment from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-an-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-an-attachment?connectionId=$CONNECTION_ID&attachmentGid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attachmentGid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-an-attachment?${params}`, {
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
| `attachmentGid` | string | yes | Asana attachment gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `GET attachments/:attachment_gid` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-attachment.md) for the provider-specific parameters and requirements.

