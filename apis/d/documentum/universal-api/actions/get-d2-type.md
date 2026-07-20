# Documentum: Get D2 Type



```
GET https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-d2-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-d2-type?connectionId=$CONNECTION_ID&repositoryName=d2repo&typeId=dm_document&profileId=0900000180001234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "repositoryName": "d2repo",
  "typeId": "dm_document",
  "profileId": "0900000180001234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/get-d2-type?${params}`, {
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
| `typeId` | string | yes | Object ID of the D2 type configuration. Example: `dm_document`. |
| `profileId` | string | yes | Object ID of the D2 creation profile that owns the type. Example: `0900000180001234`. |

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
| `id` | string | Type identifier. |
| `links[].href` | string | Type link URL. |
| `links[].rel` | string | Type link relation. |
| `title` | string | Type title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `GET /repositories/{repositoryName}/type-configuration/{typeId}` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-d2-type.md) for the provider-specific parameters and requirements.

