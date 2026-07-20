# ForceManager: Delete Company

Deletes an existing company from ForceManager.

```
DELETE https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/delete-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/delete-company?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/delete-company?${params}`, {
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
| `id` | number | yes | Unique identifier for the account. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cityName": "Ava Chen",
      "extId": "string",
      "id": 1,
      "name": "Ava Chen",
      "postcode": "string",
      "provinceName": "Ava Chen",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cityName` | string | City name. |
| `extId` | string | External id of the account from a third-party system. |
| `id` | number | Unique identifier for the account. |
| `name` | string | Name of the account. |
| `postcode` | string | Postcode of the account. |
| `provinceName` | string | Province name. |
| `vatNumber` | string | Value Added Tax identification number of the account. |

## Native endpoint

Through the native ForceManager API, this operation is `DELETE /companies`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-company.md) for the provider-specific parameters and requirements.

