# TalentHR: List Employee Available Assets

Retrieves an employee's available assets from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-available-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-available-assets?connectionId=$CONNECTION_ID&employee=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employee": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-available-assets?${params}`, {
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
| `employee` | number | yes | TalentHR employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assetCategory": {},
      "assetCategoryId": 1,
      "assetType": {},
      "assetTypeId": 1,
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetCategory` | object |  |
| `assetCategoryId` | number |  |
| `assetType` | object |  |
| `assetTypeId` | number |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /employees/:employee/available-assets` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-available-assets.md) for the provider-specific parameters and requirements.

