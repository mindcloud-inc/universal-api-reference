# Documentum: List D2 Types



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-d2-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-d2-types?connectionId=$CONNECTION_ID&repositoryName=d2repo&profileId=0900000180001234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "profileId": "0900000180001234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-d2-types?${params}`, {
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
| `profileId` | string | yes | Object ID of the D2 creation profile whose types should be listed. Example: `0900000180001234`. |

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
| `entries[].id` | string | Type entry identifier. |
| `entries[].links[].href` | string | Entry link URL. |
| `entries[].links[].rel` | string | Entry link relation. |
| `entries[].title` | string | Type entry title. |
| `entries[].updated` | date | Type entry update timestamp. |
| `id` | string | Feed identifier. |
| `title` | string | Feed title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/type-configuration` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-d2-types.md) for the provider-specific parameters and requirements.

