# eCFR: List Title Versions

Retrieves the available versions for a title from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-title-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-title-versions?connectionId=$CONNECTION_ID&title=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "title": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-title-versions?${params}`, {
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
| `title` | number | yes | CFR title number, such as 1. |
| `part` | string | no | Optional CFR part identifier to filter versions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `issueDate` | string | no | Optional issue date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_versions": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_versions` | array<object> | Version records for content in the requested CFR title. |
| `meta` | object | Version result metadata. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/versioner/v1/versions/title-:title.json` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-title-versions.md) for the provider-specific parameters and requirements.

