# Documentum: List Document Templates



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-document-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-document-templates?connectionId=$CONNECTION_ID&repositoryName=d2repo&objectId=090000018000abcd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "objectId": "090000018000abcd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-document-templates?${params}`, {
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
| `objectId` | string | yes | Documentum object ID. Example: `090000018000abcd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {
          "id": "string",
          "links": [
            {
              "href": "https://example.com",
              "rel": "https://example.com"
            }
          ],
          "title": "string",
          "updated": "2026-05-07T12:00:00.000Z"
        }
      ],
      "id": "string",
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries[].id` | string | Template entry identifier. |
| `entries[].links[].href` | string | Entry link URL. |
| `entries[].links[].rel` | string | Entry link relation. |
| `entries[].title` | string | Template entry title. |
| `entries[].updated` | date | Template entry update timestamp. |
| `id` | string | Feed identifier. |
| `title` | string | Feed title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/objects/{objectId}/document-templates` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-templates.md) for the provider-specific parameters and requirements.

