# Airzone Cloud: Get Installation

Retrieves a user's installation relation from Airzone Cloud.

```
GET https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-installation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-installation?connectionId=$CONNECTION_ID&installationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "installationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-installation?${params}`, {
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
| `installationId` | string | yes | The Airzone installation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "access_type": "string",
      "confirmation_date": "string",
      "groups": [
        {}
      ],
      "installation_id": "string",
      "location_id": "string",
      "name": "Ava Chen",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Installation relation ID. |
| `access_type` | string | User access type for the installation. |
| `confirmation_date` | string | Invitation confirmation timestamp. |
| `groups` | array<object> | Installation groups visible to the user. |
| `installation_id` | string | Installation ID. |
| `location_id` | string | Location ID for the installation. |
| `name` | string | Installation name. |
| `user_id` | string | User ID for the installation relation. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `GET /installations/{installationId}` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-installation.md) for the provider-specific parameters and requirements.

