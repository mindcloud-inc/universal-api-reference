# Damstra Forms: Get Memo

Retrieves a memo from Damstra Forms.

```
GET https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-memo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Damstra Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-memo?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/damstraForms/latest/actions/get-memo?${params}`, {
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
| `id` | number | yes | The unique identifier of the memo. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {
        "interpretationHint": 1,
        "reference": "string",
        "value": "string"
      },
      "metadata": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "creator": {
          "href": "string",
          "id": 1,
          "uuid": "string"
        },
        "href": "string",
        "id": 1,
        "owner": {
          "id": 1,
          "uuid": "string"
        },
        "project": {
          "id": 1,
          "uuid": "string"
        },
        "status": 1,
        "template": {
          "draftTemplate": {
            "href": "string",
            "id": 1
          },
          "href": "string",
          "id": 1
        },
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | array<object> | From Damstra Forms API example response. |
| `fields.interpretationHint` | number | From Damstra Forms API example response. |
| `fields.reference` | string | From Damstra Forms API example response. |
| `fields.value` | string | From Damstra Forms API example response. |
| `metadata` | object | From Damstra Forms API example response. |
| `metadata.createdAt` | date | From Damstra Forms API example response. |
| `metadata.creator` | object | From Damstra Forms API example response. |
| `metadata.creator.href` | string | From Damstra Forms API example response. |
| `metadata.creator.id` | number | From Damstra Forms API example response. |
| `metadata.creator.uuid` | string | From Damstra Forms API example response. |
| `metadata.href` | string | From Damstra Forms API example response. |
| `metadata.id` | number | From Damstra Forms API example response. |
| `metadata.owner` | object | From Damstra Forms API example response. |
| `metadata.owner.id` | number | From Damstra Forms API example response. |
| `metadata.owner.uuid` | string | From Damstra Forms API example response. |
| `metadata.project` | object | From Damstra Forms API example response. |
| `metadata.project.id` | number | From Damstra Forms API example response. |
| `metadata.project.uuid` | string | From Damstra Forms API example response. |
| `metadata.status` | number | From Damstra Forms API example response. |
| `metadata.template` | object | From Damstra Forms API example response. |
| `metadata.template.draftTemplate` | object | From Damstra Forms API example response. |
| `metadata.template.draftTemplate.href` | string | From Damstra Forms API example response. |
| `metadata.template.draftTemplate.id` | number | From Damstra Forms API example response. |
| `metadata.template.href` | string | From Damstra Forms API example response. |
| `metadata.template.id` | number | From Damstra Forms API example response. |
| `metadata.type` | string | From Damstra Forms API example response. |
| `metadata.updatedAt` | date | From Damstra Forms API example response. |
| `metadata.uuid` | string | From Damstra Forms API example response. |

## Native endpoint

Through the native Damstra Forms API, this operation is `GET /memos/{id}` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-memo.md) for the provider-specific parameters and requirements.

