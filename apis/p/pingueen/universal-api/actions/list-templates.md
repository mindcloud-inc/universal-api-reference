# Pingueen: List Templates



```
GET https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingueen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-templates?${params}`, {
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
      "category": "string",
      "components": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": {},
      "external_id": "string",
      "id": "string",
      "language": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "namespace": "Ava Chen",
      "partner_id": "string",
      "quality_score": {},
      "rejected_reason": "string",
      "status": "string",
      "updated_external": true,
      "waba_account_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Template category. |
| `components` | array<object> | Template components. |
| `created_at` | date | Template creation date. |
| `created_by` | object | Template creator information. |
| `external_id` | string | External template identifier. |
| `id` | string | Internal template identifier. |
| `language` | string | Template language code. |
| `modified_at` | date | Last modification date. |
| `name` | string | Template name. |
| `namespace` | string | Template namespace. |
| `partner_id` | string | Partner identifier. |
| `quality_score` | object | Quality score information. |
| `rejected_reason` | string | Reason for rejection, if any. |
| `status` | string | Template approval status. |
| `updated_external` | boolean | Whether the template was updated externally. |
| `waba_account_id` | string | WhatsApp Business Account ID. |

## Native endpoint

Through the native Pingueen API, this operation is `GET /user/templates` (base URL `https://api.pingueen.it/ext/v2/{{credentials.businessname}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

