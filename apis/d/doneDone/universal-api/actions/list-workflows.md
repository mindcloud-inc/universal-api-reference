# DoneDone: List Workflows

Retrieves workflows from DoneDone.

```
GET https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DoneDone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/list-workflows?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doneDone/latest/actions/list-workflows?${params}`, {
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
| `accountId` | number | yes | DoneDone account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "entityTypeID": 1,
      "id": 1,
      "isEditable": true,
      "isPublished": true,
      "listStatuses": [
        {
          "color": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `entityTypeID` | number |  |
| `id` | number |  |
| `isEditable` | boolean |  |
| `isPublished` | boolean |  |
| `listStatuses[].color` | string |  |
| `listStatuses[].id` | number |  |
| `listStatuses[].name` | string |  |
| `name` | string |  |

## Native endpoint

Through the native DoneDone API, this operation is `GET /:account_id/workflows/for-selection` (base URL `https://2.donedone.com/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

