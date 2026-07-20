# Documentum: Get Search Configuration



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-search-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-search-configuration?connectionId=$CONNECTION_ID&repositoryName=d2repo&configId=0900000180005678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "configId": "0900000180005678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-search-configuration?${params}`, {
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
| `configId` | string | yes | Object ID of the D2 search configuration. Example: `0900000180005678`. |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Search configuration identifier. |
| `links[].href` | string | Configuration link URL. |
| `links[].rel` | string | Configuration link relation. |
| `title` | string | Search configuration title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/search-configuration/{configId}` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-configuration.md) for the provider-specific parameters and requirements.

