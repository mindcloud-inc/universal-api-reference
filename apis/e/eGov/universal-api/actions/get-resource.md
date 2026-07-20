# e-Gov: Get Resource

Retrieves resource metadata from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-resource?connectionId=$CONNECTION_ID&id=1a89d4a1-905b-41ca-aeda-6f1ed55d544e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1a89d4a1-905b-41ca-aeda-6f1ed55d544e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-resource?${params}`, {
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
| `id` | string | yes | Default: `1a89d4a1-905b-41ca-aeda-6f1ed55d544e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cache_last_updated": "string",
      "cache_url": "https://example.com",
      "copyright": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "datastore_active": true,
      "datastore_contains_all_records_of_source_file": true,
      "description": "string",
      "docanlys": true,
      "format": "string",
      "hash": "string",
      "id": "string",
      "language": "string",
      "last_modified": "string",
      "last_modified_date": "2026-05-07T12:00:00.000Z",
      "license_id": "string",
      "metadata_modified": "2026-05-07T12:00:00.000Z",
      "mimetype": "string",
      "mimetype_inner": "string",
      "name": "Ava Chen",
      "package_id": "string",
      "position": 1,
      "private": "string",
      "resource_type": "string",
      "size": 1,
      "state": "string",
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
| `cache_last_updated` | string |  |
| `cache_url` | string |  |
| `copyright` | string |  |
| `created` | date |  |
| `datastore_active` | boolean |  |
| `datastore_contains_all_records_of_source_file` | boolean |  |
| `description` | string |  |
| `docanlys` | boolean |  |
| `format` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `language` | string |  |
| `last_modified` | string |  |
| `last_modified_date` | date |  |
| `license_id` | string |  |
| `metadata_modified` | date |  |
| `mimetype` | string |  |
| `mimetype_inner` | string |  |
| `name` | string |  |
| `package_id` | string |  |
| `position` | number |  |
| `private` | string |  |
| `resource_type` | string |  |
| `size` | number |  |
| `state` | string |  |
| `url` | string |  |
| `url_type` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /resource_show` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resource.md) for the provider-specific parameters and requirements.

