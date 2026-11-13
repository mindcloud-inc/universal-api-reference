# 3E Protect: Get File

Retrieves a file from the https://3eonline.com/ImageServer/ImageViewer.aspx URL

```
GET https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-file?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-file?${params}`, {
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
| `id` | string | no | The id to be added to the image URL. E.g. https://3eonline.com/ImageServer/ImageViewer.aspx?id={id} |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `GET https://3eonline.com/ImageServer/ImageViewer.aspx`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

