# Pitchbox: List Personalization Fields



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-personalization-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-personalization-fields?connectionId=$CONNECTION_ID&project.id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project.id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-personalization-fields?${params}`, {
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
| `project.id` | number | yes | Filtering by project.id |
| `campaign.id` | number | no | Filtering by campaign.id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "description": "string",
      "id": 1,
      "isSystem": true,
      "label": "string",
      "required": true,
      "token": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.id` | number |  |
| `campaign.name` | string |  |
| `campaign.status` | string |  |
| `description` | string |  |
| `id` | number |  |
| `isSystem` | boolean |  |
| `label` | string |  |
| `required` | boolean |  |
| `token` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/personalization` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-personalization-fields.md) for the provider-specific parameters and requirements.

