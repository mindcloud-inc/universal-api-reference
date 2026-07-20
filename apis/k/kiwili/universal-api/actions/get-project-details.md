# Kiwili: Get Project Details

Retrieves details for a project in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-project-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-project-details?connectionId=$CONNECTION_ID&project_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-project-details?${params}`, {
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
| `project_id` | number | yes | The Kiwili project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Archive": true,
      "EnterpriseId": 1,
      "Id": 1,
      "Name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Archive` | boolean |  |
| `EnterpriseId` | number |  |
| `Id` | number |  |
| `Name` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /project/:project_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-details.md) for the provider-specific parameters and requirements.

