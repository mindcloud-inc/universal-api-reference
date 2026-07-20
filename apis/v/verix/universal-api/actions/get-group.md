# Verix: Get Group

Retrieves a credential group from Verix.

```
GET https://connect.mindcloud.co/v1/universal/verix/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verix/latest/actions/get-group?connectionId=$CONNECTION_ID&group_id=894" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group_id": "894"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verix/latest/actions/get-group?${params}`, {
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
| `group_id` | number | yes | Numeric Verix group ID. Example: `894`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "benefits": [
        {}
      ],
      "createTime": 1,
      "creatorId": 1,
      "description": "string",
      "extraParams": {},
      "id": 1,
      "issuedRecipient": 1,
      "name": "Ava Chen",
      "subjectSchema": {},
      "templateImageRelUrl": "https://example.com",
      "totalRecipient": 1,
      "types": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `benefits` | array<object> | Benefits associated with the group. |
| `createTime` | number | Unix timestamp when the group was created. |
| `creatorId` | number | User ID of the group creator. |
| `description` | string | Group description. |
| `extraParams` | object | Additional template parameters. |
| `id` | number | Unique identifier for the group. |
| `issuedRecipient` | number | Recipients already issued credentials. |
| `name` | string | Group name. |
| `subjectSchema` | object | Schema definition for the credential subject. |
| `templateImageRelUrl` | string | Relative URL of the template image. |
| `totalRecipient` | number | Total recipients in the group. |
| `types` | object | Additional type metadata. |

## Native endpoint

Through the native Verix API, this operation is `GET /v1/credentials/groups/:group_id/` (base URL `https://api.verix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

