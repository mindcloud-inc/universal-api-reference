# Documentum: Run Quick Search



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/run-quick-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/run-quick-search?connectionId=$CONNECTION_ID&repositoryName=d2repo&searchRequest=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "searchRequest": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/run-quick-search?${params}`, {
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
| `searchRequest` | object | yes | Quick search request JSON payload. Example: `[object Object]`. |

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
          "properties": {
            "objectName": "Ava Chen",
            "objectType": "string"
          },
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
| `entries[].id` | string | Search result entry identifier. |
| `entries[].links[].href` | string | Search result link URL. |
| `entries[].links[].rel` | string | Search result link relation. |
| `entries[].properties.objectName` | string | Search result object name. |
| `entries[].properties.objectType` | string | Search result object type. |
| `entries[].title` | string | Search result title. |
| `entries[].updated` | date | Search result update timestamp. |
| `id` | string | Search result identifier. |
| `title` | string | Search result title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `POST /repositories/{repositoryName}/quickSearch` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-quick-search.md) for the provider-specific parameters and requirements.

