# Microsoft Teams: Share File



```
PUT https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/share-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/share-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveId": "string",
  "fileId": "string",
  "recipients[]": [
    {}
  ],
  "recipients[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/share-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveId": "string",
    "fileId": "string",
    "recipients[]": [{}],
    "recipients[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveId` | string | yes | Use parentReference.driveId returned by Upload Chat File. |
| `fileId` | string | yes | Use id returned by Upload Chat File. |
| `recipients[]` | array<object> | yes | All intended recipients from List Chat Members. Each recipient must have an email address. Grants read access without sending invitation emails. |
| `recipients[].email` | string | yes | Use email from List Chat Members. Do not send the chat message until access has been confirmed for every intended recipient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "grantedTo": {
        "user": {
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": "string"
        }
      },
      "grantedToV2": {
        "user": {
          "@odata": {
            "type": "string"
          },
          "displayName": "Ava Chen",
          "email": "ava@example.com",
          "id": "string"
        }
      },
      "id": "string",
      "roles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `grantedTo` | object |  |
| `grantedTo.user` | object |  |
| `grantedTo.user.displayName` | string |  |
| `grantedTo.user.email` | string |  |
| `grantedTo.user.id` | string |  |
| `grantedToV2` | object |  |
| `grantedToV2.user` | object |  |
| `grantedToV2.user.@odata.type` | string |  |
| `grantedToV2.user.displayName` | string |  |
| `grantedToV2.user.email` | string |  |
| `grantedToV2.user.id` | string |  |
| `id` | string |  |
| `roles` | array<string> |  |

## Native endpoint

Through the native Microsoft Teams API, this operation is `POST /v1.0/drives/:driveId/items/:fileId/invite` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/share-file.md) for the provider-specific parameters and requirements.

