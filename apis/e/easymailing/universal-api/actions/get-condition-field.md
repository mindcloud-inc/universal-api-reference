# Easymailing: Get Condition Field

Retrieves a condition field from Easymailing.

```
GET https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-condition-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easymailing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-condition-field?connectionId=$CONNECTION_ID&audienceUuid=string&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "audienceUuid": "string",
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easymailing/latest/actions/get-condition-field?${params}`, {
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
| `audienceUuid` | string | yes | Audience UUID. |
| `uuid` | string | yes | Condition field UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "inputType": "string",
      "multiple": true,
      "name": "Ava Chen",
      "operators": {
        "contains": "string",
        "ends": {
          "with": "string"
        },
        "is": {
          "not": "string"
        },
        "not": {
          "contains": "string",
          "ends": {
            "with": "string"
          },
          "start": {
            "with": "string"
          }
        },
        "start": {
          "with": "string"
        }
      },
      "options": {},
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `inputType` | string |  |
| `multiple` | boolean |  |
| `name` | string |  |
| `operators.contains` | string |  |
| `operators.ends.with` | string |  |
| `operators.is` | string |  |
| `operators.is.not` | string |  |
| `operators.not.contains` | string |  |
| `operators.not.ends.with` | string |  |
| `operators.not.start.with` | string |  |
| `operators.start.with` | string |  |
| `options` | object |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Easymailing API, this operation is `GET /audiences/{{audienceUuid}}/condition_fields/{{uuid}}` (base URL `https://api.easymailing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-condition-field.md) for the provider-specific parameters and requirements.

