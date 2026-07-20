# e-Gov: Get Dataset

Retrieves a dataset and its resources from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-dataset?connectionId=$CONNECTION_ID&id=moj_20180907_0008" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "moj_20180907_0008"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-dataset?${params}`, {
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
| `id` | string | yes | Dataset identifier or dataset name. Default: `moj_20180907_0008`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "author_email": "ava@example.com",
      "contactPoint": "string",
      "creator_user_id": "string",
      "distribution": "string",
      "extras": [
        {}
      ],
      "frequency_of_update": "string",
      "groups": [
        {}
      ],
      "id": "string",
      "isopen": true,
      "landingPage": "string",
      "license_id": "string",
      "license_title": "string",
      "maintainer": "string",
      "maintainer_email": "ava@example.com",
      "metadata_created": "2026-05-07T12:00:00.000Z",
      "metadata_modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "num_resources": 1,
      "num_tags": 1,
      "organization": {},
      "owner_org": "string",
      "private": true,
      "publisher": "string",
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
      "tags": [
        {}
      ],
      "temporal": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com"
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
| `contactPoint` | string |  |
| `creator_user_id` | string |  |
| `distribution` | string |  |
| `extras` | array<object> |  |
| `frequency_of_update` | string |  |
| `groups` | array<object> |  |
| `id` | string |  |
| `isopen` | boolean |  |
| `landingPage` | string |  |
| `license_id` | string |  |
| `license_title` | string |  |
| `maintainer` | string |  |
| `maintainer_email` | string |  |
| `metadata_created` | date |  |
| `metadata_modified` | date |  |
| `name` | string |  |
| `notes` | string |  |
| `num_resources` | number |  |
| `num_tags` | number |  |
| `organization` | object |  |
| `owner_org` | string |  |
| `private` | boolean |  |
| `publisher` | string |  |
| `relationships_as_object` | array<string> |  |
| `relationships_as_subject` | array<string> |  |
| `resources` | array<object> |  |
| `spatial` | string |  |
| `state` | string |  |
| `tags` | array<object> |  |
| `temporal` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /package_show` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dataset.md) for the provider-specific parameters and requirements.

