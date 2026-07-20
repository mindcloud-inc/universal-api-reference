# Leiga: List Project Issue Filter Fields

Retrieves issue filter fields for a project in Leiga.

```
GET https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-issue-filter-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leiga `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-issue-filter-fields?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-project-issue-filter-fields?${params}`, {
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
| `projectId` | number | yes | Project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "controlCode": "string",
      "customFieldCode": "string",
      "customFieldId": 1,
      "customFieldName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `controlCode` | string | Field control type. |
| `customFieldCode` | string | Field code. |
| `customFieldId` | number | Custom field ID. |
| `customFieldName` | string | Field name. |

## Native endpoint

Through the native Leiga API, this operation is `POST /issue/filter-condition-field` (base URL `https://app.leiga.com/openapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-issue-filter-fields.md) for the provider-specific parameters and requirements.

