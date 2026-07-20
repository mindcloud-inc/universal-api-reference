# e-Gov: List Datasets With Resources

Retrieves datasets with resources from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-datasets-with-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-datasets-with-resources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-datasets-with-resources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "author_email": "ava@example.com",
      "compliant_standard": "string",
      "contactPoint": "string",
      "contactPoint_email": "ava@example.com",
      "contactPoint_etc": "string",
      "contactPoint_ext": "string",
      "contactPoint_formUrl": "https://example.com",
      "contactPoint_tel": "string",
      "creator_user_id": "string",
      "distribution": "string",
      "etc": "string",
      "frequency_of_update": "string",
      "groups": [
        "string"
      ],
      "history_information": "string",
      "id": "string",
      "index_id": "string",
      "isopen": true,
      "landingPage": "string",
      "license_id": "string",
      "license_title": "string",
      "local_government": "string",
      "maintainer": "string",
      "maintainer_email": "ava@example.com",
      "metadata_created": "2026-05-07T12:00:00.000Z",
      "metadata_modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "num_resources": 1,
      "num_tags": 1,
      "opendata_id": "string",
      "organization": {},
      "owner_org": "string",
      "private": true,
      "provider_last_modified_date": "string",
      "provider_metadata_modified": "string",
      "publisher": "string",
      "related_documents": "string",
      "relationships_as_object": [
        "string"
      ],
      "relationships_as_subject": [
        "string"
      ],
      "resources": [
        {}
      ],
      "spatial": "string",
      "state": "string",
      "subtitle": "string",
      "tags": [
        "string"
      ],
      "temporal": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `author_email` | string |  |
| `compliant_standard` | string |  |
| `contactPoint` | string |  |
| `contactPoint_email` | string |  |
| `contactPoint_etc` | string |  |
| `contactPoint_ext` | string |  |
| `contactPoint_formUrl` | string |  |
| `contactPoint_tel` | string |  |
| `creator_user_id` | string |  |
| `distribution` | string |  |
| `etc` | string |  |
| `frequency_of_update` | string |  |
| `groups` | array<string> |  |
| `history_information` | string |  |
| `id` | string |  |
| `index_id` | string |  |
| `isopen` | boolean |  |
| `landingPage` | string |  |
| `license_id` | string |  |
| `license_title` | string |  |
| `local_government` | string |  |
| `maintainer` | string |  |
| `maintainer_email` | string |  |
| `metadata_created` | date |  |
| `metadata_modified` | date |  |
| `name` | string |  |
| `notes` | string |  |
| `num_resources` | number |  |
| `num_tags` | number |  |
| `opendata_id` | string |  |
| `organization` | object |  |
| `owner_org` | string |  |
| `private` | boolean |  |
| `provider_last_modified_date` | string |  |
| `provider_metadata_modified` | string |  |
| `publisher` | string |  |
| `related_documents` | string |  |
| `relationships_as_object` | array<string> |  |
| `relationships_as_subject` | array<string> |  |
| `resources` | array<object> |  |
| `spatial` | string |  |
| `state` | string |  |
| `subtitle` | string |  |
| `tags` | array<string> |  |
| `temporal` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /current_package_list_with_resources` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-datasets-with-resources.md) for the provider-specific parameters and requirements.

