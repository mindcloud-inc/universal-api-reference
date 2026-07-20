# Documentum: Get Native Annotations



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-native-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-native-annotations?connectionId=$CONNECTION_ID&repositoryName=d2repo&objectId=090000018000abcd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "objectId": "090000018000abcd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-native-annotations?${params}`, {
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
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `objectId` | string | yes | Documentum document or task object ID. Example: `090000018000abcd`. |
| `inline` | boolean | no | When true, return annotation details inline. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        {
          "content": "string",
          "id": "string",
          "type": "string"
        }
      ],
      "content": "string",
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "rel": "https://example.com"
        }
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations[].content` | string | Annotation content. |
| `annotations[].id` | string | Annotation identifier. |
| `annotations[].type` | string | Annotation type. |
| `content` | string | Native annotation content reference. |
| `id` | string | Document identifier. |
| `links[].href` | string | Annotation link URL. |
| `links[].rel` | string | Annotation link relation. |
| `title` | string | Document title. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/objects/{objectId}/native-annotations-for-collaboration-edit` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-native-annotations.md) for the provider-specific parameters and requirements.

