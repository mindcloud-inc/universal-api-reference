# Dolibarr: Get State

Retrieves a state or province from Dolibarr.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-state?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-state?${params}`, {
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
| `id` | number | yes | Dolibarr state or province ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": "string",
      "code": "string",
      "code_departement": "string",
      "id": "string",
      "name": "Ava Chen",
      "nom": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string | Active flag. |
| `code` | string | State or department code. |
| `code_departement` | string | Department code. |
| `id` | string | Dolibarr state or department id. |
| `name` | string | State or department name. |
| `nom` | string | Localized state or department name. |

## Native endpoint

Through the native Dolibarr API, this operation is `GET /setup/dictionary/states/{id}` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-state.md) for the provider-specific parameters and requirements.

