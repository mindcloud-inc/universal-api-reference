# E2B: List Template Tags

Retrieves a list of template tags from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-template-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-template-tags?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-template-tags?${params}`, {
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
| `templateId` | string | yes | Identifier of the template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buildID": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buildID` | string | Identifier of the build associated with this tag. |
| `createdAt` | date | Time when the tag was assigned. |
| `tag` | string | Tag name. |

## Native endpoint

Through the native E2B API, this operation is `GET /templates/{templateID}/tags` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-tags.md) for the provider-specific parameters and requirements.

