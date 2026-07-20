# e-Gov: Search Resources

Finds resources in e-Gov by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/search-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/search-resources?connectionId=$CONNECTION_ID&query=format%3ACSV" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "format:CSV"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/search-resources?${params}`, {
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
| `query` | string | yes | Default: `format:CSV`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order_by` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_url": "https://example.com",
      "cache_last_updated": "string",
      "cache_url": "https://example.com",
      "compliant_standard": "string",
      "copyright": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "datastore_active": true,
      "datastore_contains_all_records_of_source_file": true,
      "description": "string",
      "docanlys": true,
      "download_url": "https://example.com",
      "format": "string",
      "hash": "string",
      "id": "string",
      "last_modified": "string",
      "license_id": "string",
      "metadata_modified": "2026-05-07T12:00:00.000Z",
      "mimetype": "string",
      "mimetype_inner": "string",
      "name": "Ava Chen",
      "package_id": "string",
      "position": 1,
      "private": "string",
      "provider_last_modified_date": "string",
      "provider_metadata_modified": "string",
      "related_documents": "string",
      "resource_type": "string",
      "size": "string",
      "state": "string",
      "terms_and_conditions": "string",
      "url": "https://example.com",
      "url_type": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_url` | string |  |
| `cache_last_updated` | string |  |
| `cache_url` | string |  |
| `compliant_standard` | string |  |
| `copyright` | string |  |
| `created` | date |  |
| `datastore_active` | boolean |  |
| `datastore_contains_all_records_of_source_file` | boolean |  |
| `description` | string |  |
| `docanlys` | boolean |  |
| `download_url` | string |  |
| `format` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `last_modified` | string |  |
| `license_id` | string |  |
| `metadata_modified` | date |  |
| `mimetype` | string |  |
| `mimetype_inner` | string |  |
| `name` | string |  |
| `package_id` | string |  |
| `position` | number |  |
| `private` | string |  |
| `provider_last_modified_date` | string |  |
| `provider_metadata_modified` | string |  |
| `related_documents` | string |  |
| `resource_type` | string |  |
| `size` | string |  |
| `state` | string |  |
| `terms_and_conditions` | string |  |
| `url` | string |  |
| `url_type` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /resource_search` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-resources.md) for the provider-specific parameters and requirements.

