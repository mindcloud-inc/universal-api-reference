# ActivityInfo: Get Report

Retrieves a specific report from ActivityInfo.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-report?connectionId=$CONNECTION_ID&reportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-report?${params}`, {
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
| `reportId` | string | yes | ActivityInfo report ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": [
        {}
      ],
      "databaseId": "string",
      "id": "string",
      "label": "string",
      "layout": "string",
      "ownerId": "string",
      "ownerType": "string",
      "published": true,
      "sources": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | array<object> | Report components. |
| `databaseId` | string | Database ID when database-owned. |
| `id` | string | Report ID. |
| `label` | string | Report label. |
| `layout` | string | Report layout. |
| `ownerId` | string | Owner ID. |
| `ownerType` | string | Report owner type. |
| `published` | boolean | Whether published. |
| `sources` | object | Data sources included in the report. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/reports/:reportId` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report.md) for the provider-specific parameters and requirements.

