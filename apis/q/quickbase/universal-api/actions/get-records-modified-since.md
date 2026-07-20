# Quickbase: Get Records Modified Since

Retrieves Quickbase records modified after a specified timestamp.

```
GET https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-records-modified-since
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-records-modified-since?connectionId=$CONNECTION_ID&from=string&after=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "after": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-records-modified-since?${params}`, {
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
| `from` | string | yes | The Quickbase table identifier. |
| `after` | date | yes | ISO-8601 UTC timestamp to check for changes after. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldList[]` | array<number> | no | Optional field IDs to traverse for dependency-aware change detection. |
| `includeDetails` | boolean | no | Whether to include the individual record changes in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changes": [
        {}
      ],
      "count": 1,
      "deletesTruncated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changes` | array<object> | The individual record changes when details are included. |
| `count` | number | The number of detected changes. |
| `deletesTruncated` | boolean | Whether delete details were truncated. |

## Native endpoint

Through the native Quickbase API, this operation is `POST v1/records/modifiedSince` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-records-modified-since.md) for the provider-specific parameters and requirements.

